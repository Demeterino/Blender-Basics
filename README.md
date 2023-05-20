___
# Blender-Basics

*A small .blend for basic needs of a 3D student doing some 3D modeling.*
___
This is a "lazy-student" blender node group repository to help my friends and colleagues, there is nothing serious about it. feel free to use, maybe they'll come pretty useful someday.
#### Feature list:

* Shader editor groups:
	* Edited Principled BSDF
	* Texture mapping group node
	* Shader presets (currently mostly for Eevee):
		* watercolorLike
		* simpleToon
		* toonTexturedGradient
		* simpleToonIslands
		* Outline shader

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/shadNode.png)

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/outlineNode.png)

* Geometry node groups:
	* Mirror in Geometry node editor
	* Array in Geometry node editor
	* True/False group node for XYZ values

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/geoNode.png)

* HDRI map packed inside (Alps Field 2k resolution) with Coordinated Mapping added

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/worldConfig.png)

* Modificators on Cube (Bevel, Subdivision, Solidify(for Outline material only), Geometry nodes)

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/modif.png)

* Camera + Camera Track-To Constraint added

* Workspaces clean-up:
	* Addition and replacement of work areas 
	* Workspace arrangement:
		* Layout
		* Sculpting
		* UV Editing
		* Geometry Nodes
		* Animation
		* Scripting
		* Compositing
		* Rendering

* Render and Output settings for Cycles on GPU:

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/rendConfig.png)
![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/main/images/outConfig.png)

---
#### Notes:

* Generated/UV input line is used to switch between the two Texture Coordinate outputs. Use 0 for Geanerated and 1 for UV coordinates respectively.
* Universal/Non-Uni switches between same (universal) value input (Uni input) and vector input (axes).
* Toon and Watercolor shader group nodes need ColorRamp node right before Material Output to give color.
* Watercolorlike and Coordinated Mapping group nodes have visible image/color inputs, they are NOT used as inputs and are NOT connected to anything. They are used as titles separating or grouping different .
* Texture group nodes HAVE built in Coordinated Mapping functions (except Uni values).

* Mirror geometry node group is currently able to mirror an object once for all axes. To mirror like in the Mirror modifier, use more group nodes for needed axis. (A singular node for all 3 axes is still in the works.)
* Mirror geometry node group needs the location of a pivot object (example an empty) for mirrored movement, and the location set for Relative. 
* Array geometry node group does not have the same offset varriable as the Array modifier.
* True/False is used for aplication of 2 values to any of 3 other values (axes) for vector math.
* The Active checkmark is used as a hide/unhide button just like on the regular modificator.

* Outline material needs to be in the 2nd shader slot and the Solidify modificator in the set settings to work, thickness of the outline is put in negative values.
* Sadly, when Outline is rendered in Cycles, there is a shadow on the outlined object, which I currently don't know how to fix it. 

* Mirror_Simple_V1 is left in for past version's sake. To use the new one just find Mirror_Simple group.
---
#### Version list and Changelog:

* Ver. 1.0 = Base version
* Ver. 1.1 = Simple quality of life improvements:
	* Rewrite on some group nodes for user clarity
	* Mirror geometry node group rework
	* README rewrite. :) 
	
---
#### Credits:
* Toon, Water Color and Gradient shaders = [Kevandram](https://www.youtube.com/@kevandram)
* Cycles "friendly" Outline shader = [IkariShinji](https://blenderartists.org/t/backface-culling-doesnt-show-up-in-render/1111988/5)
* HDRI = [Alps Field](https://polyhaven.com/a/alps_field) from Poly Haven by Andreas Mischok
---
If there are any issues or ideas on what to add, contact here on GitHub, I check there from time to time.

Feel free to credit, it is very appreciated.

*Licensed under GPLv3.*
