# Path Finding Algorithm

## Dependencies and 3rdparty

### Dependencies

```
sudo apt update && sudo apt upgrade -y
sudo apt install build-essential
sudo apt install cmake
sudo apt install libcairo2-dev
sudo apt install libgraphicsmagick1-dev
sudo apt install libpng-dev
```

### IO2D

Comment these lines (from 38 to 46) in CMakeLists.txt

```
if( NOT DEFINED IO2D_WITHOUT_SAMPLES )
 add_subdirectory(P0267_RefImpl/Samples)
endif()

if( NOT DEFINED IO2D_WITHOUT_TESTS )
 enable_testing()
 add_subdirectory(P0267_RefImpl/Tests)
endif()
```

Clone and build library

```
git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
cd P0267_RefImpl
mkdir -p build && cd build
cmake ..
make
sudo make install
```

## Clone repository

```
git clone https://github.com/dihnhuunam/Path-Finding-Algorithm.git --recurse-submodules
```

## Compile and run

```
mkdir build && cd build
cmake ..
make
 ./OSM_A_star_search  
 ```
