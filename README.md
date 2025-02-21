# Resolume Fx Control with Color Picker  v.1.0

### Note: This is my first stab at TouchOSC Scripting and application to Resolume. 

## About
This project was cloned from leadonvellum's color_picker project to implement color pick for layout and RGBA control.
Link to OG Project: https://github.com/leadonvellum/TouchOSC/tree/main/color_picker

This file is meant to serve as a template for you to use alongside Resolume! To use this, you will need to have a OSC enabled for these controls to work. (OSC output enabling is done individually I believe.)

![color_picker_images](resolume_color_pick.JPG)

## Guide
### Color Picker
The first page has the layout provided by **leadonvellum** for you to test color
options for your controls. Much appreciated for the work on the color picker!
A color picker has been added to pages 2-4 for easy updating on those FX Controls. A button has been added to open the color picker.
**The color picker adds color combinations for the selected color via xy/faders are: Complementary, (2) Analogous, and (2)Triadic**

### Comp/Layer/Clip Pages:
Comp, Layout, and Clip FX pages all contain the same effects: Strobe, Hue Rotate, Delay RGB, and Colorize.
Each Effect has OSC configured to go to composition, selected layer, or selected clip, depenind which page you're on

### Color Button: 
Strobe and Colorize have an extra button: Color
The Color Button will open a color pallete which will control the RGBA levels on the selected effect, page control specific. 
# Tapping on one of the color combinations at the bottom will send that color to the xy/rgba filters!

## Modify/Add Color Control for other FX:
- Copy existing clip button. Rename the button/label/group (prefernce). 
- Set the button tag to be the name of the effect you want to control, lowercase (or whatever Resolume osc control dictates for that effect)
- Modify the local variable on line 7 to find your new group name and button name.
- Set the tab update line to update each rgba fader tag to match your buttons tag

You will need to create logic to handle the addtional button for enabling/disabling the other buttons active status
