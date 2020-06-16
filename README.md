# Android GazeDataCollectingLauncher
This app collects Front Facing Camera Frame, Gyro Sensor, Accelerometer, touch (X,Y) position whenever you touch the items in launcher.<br>
In order to process and save Front Facing Camera Frame, I delayed startingActivity by 1sec(1000ms).<br>
### Needs Modification for Others to Use
This app is based on devices which has Smallest width 410dp. I worked on Pixel 3 XL specifically.(Current Smartphones' default setting. Confirmed on Nexus 5X, 6P, Pixel XL, 2XL, 3XL, S8, S9+, S10 5G, Note 9, Note 10+. But S20+ was 384dp). <br>
So if you are using device whose Smallest width is not 410dp, you have to change layout_width values in grd_items.xml<br>
Also, if you want to change the grid layout's # of columns, consider changing values in fragment_camera2_basic.xml and grd_items.xml<br>

