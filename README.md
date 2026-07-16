# Ray_Tracing_CXX
A brute-force path tracer built entirely from scratch in pure C++; math, physics, and the C++ standard library simulating how light bounces around a 3D environment.

Features:
-Core Mechanics: Rays, vector math, and camera geometry.
-Shapes: Sphere intersection and surface normals.
-Added anti-alising and defocousing blur.

The program generates the world and outputs the result via an image in the ppm format (portable pixmap)


Build & run :
```
cmake -B build
```

then run 
```
cmake --build build --config relase

```
to output the image render we run 
```
build/raytracing.exe > image.ppm

```




