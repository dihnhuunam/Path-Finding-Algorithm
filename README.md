# Path Finding Algorithm

## Dependencies and IO2D

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

Clone repository

```
git clone --recurse-submodules https://github.com/cpp-io2d/P0267_RefImpl
cd P0267_RefImpl
```

Comment these lines (from 38 to 46) in P0267_RefImpl/CMakeLists.txt

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
mkdir -p build && cd build
cmake ..
make
sudo make install
```

## Clone Path-Finding-Algorithm

```
git clone https://github.com/dihnhuunam/Path-Finding-Algorithm.git --recurse-submodules
```

## Compile and run

```
cd Path-Finding-Algorithm
mkdir build && cd build
cmake ..
make
./PathFinding
 ```
