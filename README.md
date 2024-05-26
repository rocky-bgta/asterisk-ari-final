Remove-Item -Recurse -Force build

rm -rf build
mkdir build
cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=C:/vcpkg/scripts/buildsystems/vcpkg.cmake
cmake --build .