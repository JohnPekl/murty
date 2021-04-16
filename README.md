# murty

Python package for Murty's algorithm. 

## Requirements

- Python 3.7
- Eigen 3.3
-    [install and use eigen3 on ubuntu 16.04](https://kezunlin.me/post/d97b21ee/) `sudo apt-get install libeigen3-dev` libeigen3-dev is installed install to `/usr/include/eigen3/` and `/usr/lib/cmake/eigen3`. Thus, we must make a change in **CMakeLists.txt** `SET( EIGEN3_INCLUDE_DIR "/usr/local/include/eigen3" )` to `SET( EIGEN3_INCLUDE_DIR "/usr/include/eigen3/" )`.
-    Change your Python executable in **setup.py** line #49 from `'-DPYTHON_EXECUTABLE=' + '/usr/local/opt/python/bin/python3.7']` to `'-DPYTHON_EXECUTABLE=' + '/home/computer/Desktop/python3/bin/python3']`. Here, `/home/computer/Desktop/python3/bin/python3']` is your virtual environment Python folder.

## Usage

Just type `make` and it will initiate the pybind submodule
and install the package.

You could also do 
```
git clone --recursive git@github.com:erikbohnsack/murty.git 
pip3 install ./murty
``` 

## Test

`make test`

## Acknowledgements

This code is just an extraction of Jonatan Olofsson's
implementation of Murty's algorithm from his [MHT repo](https://github.com/jonatanolofsson/mht). 
It's basically Jonatan's code implemented as [pybind's cmake_example](https://github.com/pybind/cmake_example)

## License

GPLv3
