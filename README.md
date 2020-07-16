# Setting Up Your C++ Dev Env

1. [MacOS]()
2. [Windows]()
3. [Linux]()
4. Using Your Compiler (optional)


## MacOS

If you are a Mac user,you have to download **Xcode**. 

[Download Xcode here](https://apps.apple.com/us/app/xcode/id497799835?mt=12)

You will be prompted to open the Apple Store, go there and install Xcode.

Installing Xcode will set you up with gcc/clang for compiling. 

**If you prefer to use a different IDE you are welcome to, but you will still need to install Xcode**

Please note if you choose to use a different IDE the amount of support the Instructors can offer you is limited.

### Getting Started with Xcode

To create a new project. Go to File menu -> select New -> select Project. This will create a new project for you.

Now in the next window you have to choose a template for your project. To choose a C++ template choose Application option which is under the OS X section on the left side bar. Now choose **command-line tools** from available options and hit Next button.

On the next window provide all the necessary details like ‘name of organisation’, ‘Product Name’ etc. But make sure to choose the language as C++ . After filling the details hit the next button to proceed to further steps.

Choose the location where you want to save your project. After this choose the main.cpp file from the directory list on the left side-bar.

Now after opening the main.cpp file, you will see a pre written "Hello World" c++ program. You may change this program as per your requirement. To run your C++ program you have to go to Product menu and choose the Run option from the dropdown.


## Windows

For Windows users, we recommend you install and use **Visual Studio 2019**

- [Download Visual Studio 2019](https://visualstudio.microsoft.com/downloads/)

You are welcome to use another IDE but please note that using an unsupported IDE will mean the Instructional staff can only offer limited help if you run into issues.

When installing Visual Studio be sure to select the **Desktop Development in C++** option under Workloads:

![VS2019-options](https://user-images.githubusercontent.com/40476562/87713294-d0134b00-c75e-11ea-8f91-28b76a7c98fa.png)

NOTE: If you have already installed Visual Studio and didn't select the "Desktop Dev with C++" option you will need to repair/modify your installation

Control Panel -> Add/Remove Programs -> Visual Studio -> Modify/Repair


## Linux

We will install the GNU GCC compiler on Linux.

You have to first run the below two commands from your Linux terminal window:
```
sudo apt-get update
sudo apt-get install GCC
```
This command will install the GCC compiler on your system. You will also need to run the command below:

```
sudo apt-get install build-essential
```

This command will install all the libraries which are required to compile and run a C++ program.

After completing the above step, you should check whether the GCC compiler is installed in your system correctly or not. To do this you have to run the followng command from Linux terminal:

```
g++ --version
```

## Using Your Compiler

If you have completed the above steps (for MacOS/Linux) without any errors, then your dev environment is set up and ready to be used! 

In further steps, we will learn how to compile and run a C++ program using the GCC compiler.

Write your program in a text file and save it with any file name and.CPP extension. 

Example: We have written a program to display “Hello World” and saved it in a file with the filename “helloworld.cpp” on desktop.

```cpp
#include <iostream>

int main(int argc, const char * argv[]) {
    std::cout << "Hello, World!\n";
    return 0;
}
```

Now you have to open the terminal and move to the directory where you have saved your file. 

Then you have to run the below command to compile your file:

```
g++ filename.cpp -o <name>
```

`filename.cpp` is the name of your source code file. In our case, the name is `helloworld.cpp` and <name> can be any name of your choice. This name will be assigned to the executable file which is created by the compiler after compilation. In our case, we chose <name> to be “hello”.

We will run the above command as:

```
g++ helloworld.cpp -o hello
```

After executing the above command, you will see a new file is created automatically in the same directory where you have saved the source file and the name of this file is the name you chose as <name>.

Now to run your program you have to run the below command:

```
./hello
```

This command will run your program in the terminal window.
