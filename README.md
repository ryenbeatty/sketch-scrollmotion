# sketch-scrollmotion
A plugin for Sketch to export designs as a ScrollMotion applet.

#### BEWARE: This experimental and is in no way supported by ScrollMotion. Use at your own risk: save often, keep backups of your files, and think about what you will do with all the time you've rediscovered.

## Installation
You can [Download Zip](https://github.com/jonmmay/sketch-scrollmotion/archive/master.zip) to the right and double-click on the .sketchplugin file to install.

## How to use it
* Run this plugin from the Plugins menu or by using the `Control + S` hotkey to export your layers overlays in an applet
  * Layers are exported as image or text overlay. Additional overlay types are supported using a set of specific identifier
  * Artboards are exported as pages within a single pageset
  * Images will be named based on the layer name and will be exported at @1x and @2x for retina devices
  * The plugin will request the location of custom fonts but will default to "Arial" for missing fonts
* The resulting applet will be saved in the same directory of your Sketch file
* Simply zip the applet folder and change the file extension from `zip` to `scrollmotiontransit` and upload into your WorkCloud account
* Publish your applet or make it more awesome using SmartStudio!

## Get interactive
* Identify a layer as a button with touch states by appending `[btn]` to the layer name
![](https://github.com/jonmmay/sketch-scrollmotion/blob/master/cgbutton_example.png)
![](https://github.com/jonmmay/sketch-scrollmotion/blob/master/cgbutton_example2.png)
![](https://github.com/jonmmay/sketch-scrollmotion/blob/master/imagebutton_example.png)

* Identify a layer as a container that scrolls by appending `[]` to the layer name

## Ignore me please
* Ignore a layer by appending `-` to the layer name. The plugin will work around the layer so you don't have to delete your art
  * Ignoring a layer will ignore all layers in the layer group
* Flatten a layer by appending `[flat]` to the layer name. The plugin will export the layer and sublayers as a flat bitmap. I'm working on supporting `*` as an alternative.
  * You cannot flatten an Artboard

## Known issues and shortcomings :(
* Not all Sketch layers are supported. This plugin has not been tested with slice layers, symbols, or text styling
* Not all Sketch layer properties are supported. This plugin has not been tested with transform, rotate, shadows, gaussian blur and other similar properties
* Artboard are not validated. All artboards are currently assumed to be 1024 x 768 and landscape
* Found fonts are not validated. Be mindful of the fonts that are requested
* Some text properties are not translated to the applet. Underline, super and sub script, text fills, text borders, and transparency are ignored.
* Mask layers will be exported. These will have to be deleted in SmartStudio

I will be squashing these issues and others reported here so stop by often for updates!


