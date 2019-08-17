port of Adobe XMP SDK to work on only MSVC 14 

cd build\vc14

-DXMP_BUILD_STATIC=OFF -- dynamic

-DXMP_BUILD_STATIC=ON -- static

cmake .. -L -DCMAKE_CL_64=ON -DXMP_BUILD_WARNING_AS_ERROR=OFF -DXMP_BUILD_STATIC=OFF -DGENERATORARCHITECTURE=Win64 -DCMAKE_ARCH64BIT=ON -DCMAKE_ARCH=x64 -G"Visual Studio 14 2015" -Ax64 -DCMAKE_CONFIGURATION_TYPES="Debug;Release"

Release

cmake --build . -- /p:Configuration="Release" /p:Platform="x64" /nologo /p:BuildInParallel=true /t:ReBuild

Debug

cmake --build . -- /p:Configuration="Debug" /p:Platform="x64" /nologo /p:BuildInParallel=true /t:ReBuild


 -- public\libraries
