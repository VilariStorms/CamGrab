# To build with cmake is just the usual. 
```
mkdir build 
cd build 
cmake ..
cmake --build .
```
To compile with cl.exe directly:
```
cl CommandCam.cpp ole32.lib strmiids.lib oleaut32.lib
```

Run the outputed executable with no args from the commandline to take a single bmp image from the webcam

