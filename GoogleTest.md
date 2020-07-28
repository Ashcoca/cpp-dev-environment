# Setting Up Google Test & Google Mock

We will be using Google Test as our unit test framework and mocking library.

## Getting Started

Review the [Google Test Primer](https://github.com/google/googletest/blob/master/googletest/docs/primer.md) documentation to get familiar with this framework.

We will also be using Google Mock, which is an extension to Google Test for writing and using C++ mock classes. See the separate [Google Mock documentation](https://github.com/google/googletest/blob/master/googlemock/README.md).

More detailed documentation for googletest is available [googletest/README.md](https://github.com/google/googletest/blob/master/googletest/README.md).

## Installation

1. [MacOS/Linux]()
2. [Windows (Visual Studio)]()


### MacOS

You will need to have [CMake installed](https://cmake.org/) if you do not already have it.

```
brew install cmake
```

First we'll need to download the GoogleTest repository. 

```
cd ~/  
git clone https://github.com/google/googletest
```

Next we'll navigate into the cloned `googletest` directory and create a `build` folder.

```
cd googletest
mkdir build
cd build
```

Now we'll run cmake.

```
cmake .. -DCMAKE_CXX_STANDARD=17
make
make install
```

We're almost finished! Finally we'll set our path variables. If you're using `zsh` replace `.bash_profile` with `.zshrc`

```
echo "export CPLUS_INCLUDE_PATH=/usr/local/include" >> ~/.bash_profile
echo "export LIBRARY_PATH=/usr/local/lib" >> ~/.bash_profile
 
source ~/.bash_profile 
```

The above commands create two environment variables (CPLUS_INCLUDE_PATH and LIBRARY_PATH). The first points to the location where all the system libraries are installed, this is where the header files for Google Test are. The second points to the location that all the shared libraries are installed on OS X.

During our previous set, parts of Google Test was installed between these two directories.

### Windows

Visual Studio 2019 (With the Desktop Development in C++ Workload) comes with GoogleTest.

This means if you need to add GoogleTest/GoogleMock to a project it's easy!


1. Go to 'Manage NuGet Packages' in your Solutions Explorer

![Install NuGet packages in Visual Studio4](https://user-images.githubusercontent.com/40476562/88592748-59eece00-d013-11ea-8d86-b0a0a04b87f1.png)

2. Click Browse and search for "Gmock" or "GoogleMock".

3. Select this package and install (this will install both GoogleTest and GoogleMock).

![Image Pasted at 2020-7-6 13-10](https://user-images.githubusercontent.com/40476562/88592921-9cb0a600-d013-11ea-8984-cacc213c7159.png)
