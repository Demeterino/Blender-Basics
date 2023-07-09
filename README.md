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
		* Water Shader
		* Grass Shader
		* Outline Shader
		* Hair Shader

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/shadNode.png)

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/outlineNode.png)

* Geometry node groups:
	* Mirror
	* Array
	* Rotating Array
	* Curve Geometry
	* True/False group node for XYZ values and a variant for vectors
	* To From Geometry Switch

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/geoNode.png)

* Grass and Hair Generators

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/geoNode.png)

* HDRI map packed inside (Alps Field 2k resolution) with Coordinated Mapping added
* Dual HDRI setup fo lighting and background difference in a scene, with only packed HDRI image set

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/worldConfig.png)
![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/dualConfig.png)

* modifiers on Cube: Bevel, Subdivision, Solidify(for Outline only), Main Geometry node output, Grass Generator and Hair Generator

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/modif.png)
![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/grassModif.png)
![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/hairModif.png)

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

![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/rendConfig.png)
![Screenshot](https://github.com/Demeterino/Blender-Basics/blob/Version-1.5/images/outConfig.png)

---
#### Notes:

* Generated/UV input line is used to switch between the two Texture Coordinate outputs. Use 0 for Generated and 1 for UV coordinates respectively.
* Universal/Non-Uni switches between same (universal) value input (Uni input) and vector input (axes).
* Toon and Watercolor shader group nodes need ColorRamp node right before Material Output to give color.
* Watercolorlike and Coordinated Mapping group nodes have visible image/color inputs, they are NOT used as inputs and are NOT connected to anything. They are used as titles separating or grouping different .
* Texture group nodes HAVE built in Coordinated Mapping functions (except Uni values).
* For Water flow animation use Waviness, but only for 2D planes, otherwise the water shrinks on Z axis.
* Caustic Layers go from larger to smaller caustic size, with Layer 1 being the biggest.
* Seasonal Color slider goes from Green, to Yellow, to Orange and ends at Beige.
* Ground Location, Rotation and Scale change color gradient of modeled grass straw, from bottom upward (bottom is dark).
* WB/Color switches between having and not having Seasonal Color applied to shader.

* Outline material needs to be in the 2nd shader slot and the Solidify modifier in the set settings to work, thickness of the outline is put in negative values.
* Sadly, when Outline is rendered in Cycles, there is a shadow on the outlined object, which I currently don't know how to fix it.
* Hair Shader can have both a generated texture or an image texture, for which, there are presets made that then have to be added to the Edited BSDF note as color.
* Hair Shader need a separate UV map made for it to work with Hair Generator.

* Mirror Geometry Node group is currently able to mirror an object once for all axes. To mirror like in the Mirror modifier, use more group nodes for needed axis. (Development of a singular node for all 3 axes is put on hold.)
* Mirror Geometry Node group needs the location of a pivot object (example an empty) for mirrored movement, the location has to be set for Relative. 
* Array Geometry Node group works similarly to Array modifier, the group duplicates's movement is based on physical dimensions of the mesh. To have mesh duplicates right next to each other, put value of the need axis on 1 or -1 depending on direction.
* Making a circle of chosen model with Rotating Array Geometry Node group works only on models, whose origin is set as the rotation mid point, otherwise the mesh is rotating on itself.
* Curve Geometry Geometry Node group works similarly to Curve modifier, it needs a curve on which to base the curved movement.
* True/False is used for application of 2 values to any of 3 other values (axes) for vector math.
* To From Geometry Switch Geometry Node group helps to choose weather or not the generated mesh can applied within the set parameters based on an index, that can be edited with an Additive value.
* The Active checkmark is used as a hide/unhide button just like on the regular modifier.

* Grass and Hair Generators use menus in Modifier Properties panel.
* For Hair Generator it is needed to use Hair Shader or a variation of it and or it's setup to give material to it's instances. Grass Generator does not need that, it works with meshes and does not give material to its instances.
* Grass and Hair Generators need objects in a collection to generate instances. Grass Generator generates instances of a mesh or meshes to create grass, and Hair Generator generates instances of a curve or curves to create hair.
* Grass Wind animation can be automated by giving the Frame input a driver (#frame) to move while animation plays.
* For Normal Name/Attribute of both generators, it is possible to simply use a single character as a name/attribute.

---
#### Version list and Changelog:

* Ver. 1.5 = Touch some Grass
	* Added Shader Presets: Water, Grass and Hair
	* Added Dual HDRI preset
	* Added Geometry Node Generators for Grass and Hair
	* Added Geometry Node Groups: Rotating Array, Curve Geometry, and To From Geometry Switch
	* Rework of Array and slight rework of Mirror
	* Removed [HDRI](https://polyhaven.com/a/alps_field) and previous versions of Mirror and Array Geometry Node Groups because of file size
	* README rewrite, again. :D
* Ver. 1.1 = Simple quality of life improvements:
	* Rewrite on some group nodes for user clarity
	* Mirror Geometry Node group rework
	* README rewrite. :) 
* Ver. 1.0 = Base version
	
---
#### Credits:
* Toon, Water Color and Gradient shaders = [Kevandram](https://www.youtube.com/@kevandram)
* Cycles "friendly" Outline shader = [IkariShinji](https://blenderartists.org/t/backface-culling-doesnt-show-up-in-render/1111988/5)
* Rotate Instances = [Glen Larsen](https://blender.stackexchange.com/questions/275658/geometry-nodes-how-to-rotate-multiple-instances)
* Hair Instances = [Joey Carlino](https://www.youtube.com/watch?v=9NM9oaijmLg)
* Water Shader = [Chuck CG](https://www.youtube.com/watch?v=0SJ-__0gK_k)
* Water Caustics = [Hayden Gray](https://www.youtube.com/watch?v=6LIEUQ-tTHw)
* Grass Rotation = [maurício heberle](https://www.youtube.com/watch?v=6ATWYNETZ7g)
* Grass Movement = [いわぶり(iwaburi)](https://www.youtube.com/watch?v=d6oINqiETVo)
* Curve = [Robin Betts](https://blender.stackexchange.com/questions/245282/how-to-bend-geometry-with-geometry-nodes/245553#245553)
---
If there are any issues or ideas on what to add, contact here on GitHub, I check there from time to time.

Feel free to credit, it is very appreciated.

Built in Blender 3.5.1, Tested in 3.6 LTS

*Licensed under GPLv3.*
