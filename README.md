___
# Blender-Basics

### A small .blend for basic needs of a 3D student doing some 3D modeling.
___
This is a "lazy-student" blender node group repository to help my friends and colleagues, there is nothing serious about it. feel free to use, maybe they'll come pretty useful someday.
#### Feature list:

* Shader editor groups:
	* Edited Principled BSDF points
	* Texture mapping group node
	* Shader presets (currently for Eevee

* Geometry node groups:
	* Mirror in Geometry node editor
	* Array in Geometry node editor
	* True/False group node for XYZ values

* HDRI map packed inside

* Modificators on Cube (Bevel, Subdivision, Solidify(for Outline material only), Geometry nodes)

* Camera + Camera Track-To ready

* Workspaces clean-up

---
Notes:

* Generated/UV input line is used to switch between the two Texture Coordinate outputs. Use 0 for Geanerated and 1 for UV coordinates respectively.
* Mirror geometry node group can only be used on a cloned or instanced geometry, not as an actual modifier of the geometry it was put on.
* Mirror geometry node group is currently able to do one axis per group node (a singular node for all 3 axes is in the works).
* Mirror geometry node group needs the location of the mirrored object, and a pivot object (or an empty) for mirrored movement. 
* The Active checkmark is used as a hide/unhide button just like on the regular modificator.
* Array geometry node group does not have the same offset varriable as the Array modifier.
* Toon shader group nodes need ColorRamp node right before surface input.
* Outline material needs to be in the 2nd slot and the Solidify modificator in the set settings to work, thickness of the outline is put in negative values.
* Sadly, when Outline is rendered in Cycles, there is a shadow on the outlined object, which I currently don't know how to fix it. 

---
Credits:
* Toon, Water Color and Gradient shaders = [Kevandram](https://www.youtube.com/@kevandram)
* Cycles "friendly" Outline shader = [IkariShinji](https://blenderartists.org/t/backface-culling-doesnt-show-up-in-render/1111988/5)
---
If there are any issues or ideas on what to add, contact here on GitHub in the issues tab, I check there from time to time.

Feel free to credit, it is very appreciated.

*Licensed under GPLv3.*
