# Meyer Mapp 3D - Reference Notes

## Importing Venues into Mapp 3D
*ugh. there's no good way to import venues into Mapp 3D from Vectorworks. Tips and instructions for drawing venues are below.

## Tips for Drawing Venues
* When in the model view using the view presets in the top left will restrict your drawing and object movement to the planes you are viewing.
	* ie. Left View restricts your movement to the Z and X axes.
* Tools can be accessed from the Tools menu of your OS toolbar, in the tools icons on the right of Mapp, and/or by right-clicking in the model view. A lot are available in all but some are only available in one or two, and some can only be available contextually depending on what you have selected in the model view. When you can't at first find a tool look in all the places and make sure you are clicking on the object when you right-click.
* Multi-level visual Aid allows input with distance and angle from a Lazer Disto, and Free Draw Geometry allows input with XYZ coordinates.
* After a surface is drawn you turn it into an audience surface that will be predicted by giving it an offset from the Object Settings tab.

## Drawing a Venue using a Lazer Disto
1. Open Mapp 3D and create a new file.
2. Navigate to File > Project Properties
   	* On the Units tab you can change units to your desired units.
   	* Under Environment change the Axis limits to be larger than you intend to draw. 50' extra on each axis is a good idea.
   	* Under the SPL tab you can change your Measurement Units from SPL to Attenuation. Attenuation shows the value decreasing from maximum and can be easier to look at when trying to achieve consistent tonality and level. If evaluating system headroom using SPL for your Measurement Units will be more useful.
4. Navigate to Insert > Multi-Level Visual Aid.
5. In the Multi-Level Visual Aid menu input your measurements of laser position and distance/angle of your audience plane.
6. Click apply then right-click your plane and use Modify > Extrude to extrude the surface horizontally(Y-axis).
7. Select the object then navigate to the Object Settings tab and give it an offset to represent audience height.

## Drawing a Venue from a Section Drawing
1. Do Steps 1 to 4 from Drawing a Venue using a Lazer above.
2. Navigate to Insert > Free Draw Geometry.
3. In the Free Draw Geometry Menu input your measurements of laser position and distance/angle of your audience plane.
4. Click apply then right-click your plane and use Modify > Extrude to extrude the surface horizontally(Y-axis).
5. Select the object then navigate to the Object Settings tab and give it an offset to represent audience height.

## Adjusting Array Angles
1. Select Left View or Right View in the view presets accessible in the top left corner.
2. Right-click on the source and enable center lines. This will show the box's "Impact Points".
3. Select the source by left-clicking on it in the model view or by selecting it under the Loudspeaker System list in the left toolbar.
4. Click the Express Settings tab in the left toolbar.
5. In Express Settings you can adjust box angles while looking at their impact points on the audience area.
6. Switch to an isometric view and predict to see your work! 

## Exporting Systems Into Vectorworks from Mapp 3D
1. File > Import > Import Single DXF/DWG
2. Navigate to and open file
3. Import using **Meters**
4. Tools > Organization: Design Layers Tab > Scale
	* make sure to set the scale of the imported layer to the scale you're working at

## Things to keep in mind
* Mapp 3D exports in meters, regardless of your project settings
* Mapp 3D uses the "Rotation Point" to denote box aiming.
	* What is typically called "Horizontal Angle" is manipulated via the Z-axis.
 	* What is typically called "Vertical Angle" or "Frame Angle" is manipulated via the Y-axis. The value in mapp is inverse most programs and your inclinometer. ie. -10 in Mapp would be a +10 frame angle on your array.
