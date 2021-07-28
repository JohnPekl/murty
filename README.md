# murty

Python package for Murty's algorithm. 

## Requirements

- Python 3.7
- Eigen 3.3
-    [install and use eigen3 on ubuntu 16.04](https://kezunlin.me/post/d97b21ee/) `sudo apt-get install libeigen3-dev` libeigen3-dev is installed install to `/usr/include/eigen3/` and `/usr/lib/cmake/eigen3`. Thus, we must make a change in **CMakeLists.txt** `SET( EIGEN3_INCLUDE_DIR "/usr/local/include/eigen3" )` to `SET( EIGEN3_INCLUDE_DIR "/usr/include/eigen3/" )`.
-    Change your Python executable in **setup.py** line #49 from `'-DPYTHON_EXECUTABLE=' + '/usr/local/opt/python/bin/python3.7']` to `'-DPYTHON_EXECUTABLE=' + '/home/computer/Desktop/python3/bin/python3']`. Here, `/home/computer/Desktop/python3/bin/python3']` is your virtual environment Python folder.
-    **Install in Windows 10**: (1) Download [Eigen3](https://eigen.tuxfamily.org/) release from its official website. (2) Extract that file (eg. zip) to somewhere (`C:/Eigen3`, for example). (3) Inside that folder, create another directory which we will call 'build_dir'. (4) `cd build_dir`. (5) `cmake source_dir`, make sure to install `cmake` in Windows or using `pip install cmake`, `conda install -c anaconda cmake` in your Python environment.

## Usage

Just type `make` and it will initiate the pybind submodule
and install the package.

You could also do 
```
git clone --recursive https://github.com/JohnPekl/murty.git
python setup.py build develop
``` 

## Test

`make test`

## Acknowledgements

This code is just an extraction of Jonatan Olofsson's
implementation of Murty's algorithm from his [MHT repo](https://github.com/jonatanolofsson/mht). 
It's basically Jonatan's code implemented as [pybind's cmake_example](https://github.com/pybind/cmake_example)

## License

GPLv3
