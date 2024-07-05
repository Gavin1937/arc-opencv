# arc-opencv

## cmake build flags

### opencv-490-win64-msvc-no-world.zip
```sh
cmake -S opencv-4.9.0 -B build_opencv_no_world \
    -DCMAKE_BUILD_TYPE=RelWithDebInfo \
    -DBUILD_PERF_TESTS:BOOL=OFF -DBUILD_TESTS:BOOL=OFF -DBUILD_DOCS:BOOL=ON \
    -DBUILD_opencv_world=OFF \
    -DWITH_FFMPEG=ON -DWITH_EIGEN=ON -DBUILD_JAVA=OFF -DBUILD_opencv_python2=OFF -DBUILD_opencv_python3=OFF \
    -DOPENCV_ENABLE_NONFREE=ON -DPARALLEL_ENABLE_PLUGINS=ON \
    -DOPENCV_EXTRA_MODULES_PATH="opencv_contrib-4.9.0/modules"
```

### opencv-490-win64-msvc.zip
really simular to opencv-490-win64-msvc-no-world.zip, but I forget the exact command.

### opencv-490-deb64-gcc-glibc.zip
```sh
cmake -S . -B build -DCMAKE_BUILD_TYPE=RelWithDebInfo -DBUILD_PERF_TESTS:BOOL=OFF \
    -DBUILD_TESTS:BOOL=OFF -DBUILD_DOCS:BOOL=ON -DOPENCV_ENABLE_NONFREE=ON -DPARALLEL_ENABLE_PLUGINS=ON \
    -DOPENCV_EXTRA_MODULES_PATH=/opencv/opencv_contrib-${VERSION}/modules/
```
