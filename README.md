# Android GazeDataCollectingLauncher
This app collects Front Facing Camera Frame, Gyro Sensor, Accelerometer, touch (X,Y) position whenever you touch the items in launcher. In order to process and save Front Facing Camera Frame, I delayed starting new Activity by 1sec(1000ms). Otherwise you will face errors such as Camera Handler trying to send message to dead thread.
### Needs Modification for Others to Use
This app is based on devices which has Smallest width 410dp. I worked on Pixel 3 XL specifically.(Current Smartphones' default setting. Confirmed on Nexus 5X, 6P, Pixel XL, 2XL, 3XL, S8, S9+, S10 5G, Note 9, Note 10+. But S20+ was 384dp). <br>
So if you are using device whose Smallest width is not 410dp, you have to change layout_width values in grd_items.xml<br>
Also, if you want to change the grid layout's # of columns, consider changing values in fragment_camera2_basic.xml and grd_items.xml<br>
If installed app captures Rear camera image, then you have to change the value at <br>Camera2BasicFragement.java Line 908~ if (mCameraId.equals("1")) ...... check what number equals to your device's front camera.
### Frame Resolution
My app's default Capturing frame resolution is 640x480.<br>
You can change this setting by modifying <br>Camera2BasicFragement.java Line 569: mImageReader = ImageReader.newInstance(480, 640, ImageFormat.JPEG, /*maxImages*/2);<br>
