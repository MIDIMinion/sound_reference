# Cameras (that don't suck) - Reference Notes (also monitors)

A place to put notes about good cameras, lenses, and useful info

## Cameras
* Marshall CV343-CSB
    * SDI & CVBS outputs
* Marshal CV345-CS
    * SDI & HDMI outputs
* Panasonic WV-CP-630
    * composite video
    * Day/Night capable
    * auto-focus
    * NOT TRUE IR
        * IR cut filter switches on/off to enhance sensitivity in BW mode
* Panasonic WV-CP500
    * composite video
    * Day/Night capable
    * auto-focus
    * NOT TRUE IR
        * IR cut filter switches on/off to enhance sensitivity in BW mode
* Ikegami ICD-47
    * low light, high IR sensitivity camera


## Lenses
* Rainbow L5-50mm 1:1.45 CS
    * use case: FOH shot
* GVI Security GV-5-100ADC 5-100mm f1.8
    * use case: FOH shot w/ super zoom!
* Computar 2.8-12mm 1:1.3 IR 1/3" CS
    * use case: MD Camera
* Panasonic WV-LZA61/2S
    * use case: FOH IR from middle of the house

## Monitors
* Delvcam DELV-SDI-7.7"
    * SDI, composite, & HDMI
* Boland LVB series
    * SDI, DVI, HDMI, CVBS, etc.
* Sharp LCD monitor
    * Masque barcode: 5735071861

### Monitor Hardware
* Masque and Sound Associates have [The Light Source "candy canes"](https://www.thelightsource.com/products/plasma-universal-mount-set-93) for hanging LCD tvs from battens and balcony rails.
    * Masque barcode number: 7245086781
* Masque's "X-Ray Hanggars" (code 5740)
    * great for mounting monitors. these + long vesa screws + fender washers let you put two sidearm T's on top of the monitor
    * don't forget to ask lighting for 2 side arms + T's per monitor you want to hang
        * you'll have side arms left over, but that's fine

# Camera Settings

## Marshall CV343-CSB (color)
* Lens: DC Iris
* WB Control: ATW
* AE Control:
    * Mode: Shutter
    * Brightness: 4
    * AGC Limit: 10
    * Shutter: Manual
        * Speed: 1/90 to 1/150
    * DSS: Manual
    * Backlight
        * all off
    * Day/Night: Color
    * Image Stabilizer: Off
    * Image Control
        * all default
    * Display Control
        * all default

## Marshall CV343-CSB (night)
* Lens: DC Iris
* WB Control: ATW
* AE Control:
    * Mode: Shutter
    * Brightness: 4
    * AGC Limit: 10
    * Shutter: Manual
        * Speed: 1/180
    * DSS: Manual
    * Backlight
        * all off
    * Day/Night: Color
    * Image Stabilizer: Off
    * Image Control
        * all default
    * Display Control
        * all default

## Panasonic WV-CP500 (color)
* Camera
    * ALC/ELC
        * Super-D5: ---
        * Level: +20
    * Shutter: 1/250
    * AGC: Off/Low (depends on how bright/dynamic the lighting in the show is)
    * Sense Up: ---
    * White Bal: ATW1
    * DNR: HIGH
    * BW Mode: off

## Panasonic WV-CP500 (B/W)
* Camera
    * ALC/ELC
        * Super-D5: ---
        * Level: -20
    * Shutter: 1/250
    * AGC: Off
    * Sense Up: ---
    * White Bal: ATW1
    * DNR: HIGH
    * BW Mode: on

## Ikegami ICD-47 (IR mode)
* *rent one of these and play with settings, then record here*

# Show Cameras & Settings

## Black No More Cameras
* FOH Color & IR
    * Model: Marshall CV345-CS
    * Lens: Rainbow L5-50mm 1:1.45 CS
* MD Camera
    * Model: Marshall CV343-CS
    * Lens: Computar 2.8-12mm 1:1.3 IR 1/3" CS

## Black No More Settings
* Lens: DC Iris
* WB Control: ATW
* AE Control:
    * Mode: Shutter
    * Brightness: 0
    * AGC Limit: 10
    * Shutter: Manual
        * Speed: 1/150
    * DSS: Manual
    * Backlight
        * Backlight: off
        * ACE: off
        * Eclipse: off
* Day Night: (color or night preference)
* Image stabilizer: off
* image control:
    * all default
* display control:
    * all default

### Harmony Cameras
* FOH Color: Marshal 343-CSB
    * Lens:
* FOH IR: Panasonic WV-CP500
    * Lens: Panasonic WV-LZA61/2S
* MD Cam: Panasonic WV-CP500
    * Lens: 

### Harmony IR Settings
* ALC/ELC
    * Super-D5: Off
    * Level: +20
    * Manual ABS:
* Shutter: 1/100
* AGC: On (High)
* Sens Up: Off
* White Bal: ATW
    * default settings (0)
* DNR: HIGH
* BW Mode: Auto1
    * Level: High
    * Duration Time: L
    * Burst(BW): Off

### Harmony Color Settings
* Lens: DC Iris
* WB Control: ATW
* AE Control:
    * Mode: Shutter
    * Brightness: 0
    * AGC Limit: 10
    * Shutter: Manual
        * Speed: 1/190
    * DSS: Manual
    * Backlight
        * Backlight: off
        * ACE: off
        * Eclipse: off
* Day Night: (color or night preference)
* Image stabilizer: off
* image control:
    * all default
* display control:
    * all default



## Misc. Camera & Monitor Notes
* on Harmony, the MD cam was a marshall 343-csb, and we believe it added some latency in the MD monitors (pelco 19"). When we swapped it with a panasonic wv-cp500, the delay went away.
* on Merrily We Roll Along, we learned that setting the shutter faster than 1/250 made all of the LED units appear to strobe onscteen
