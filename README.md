# Remote desktop
## Introduction
Hello everyone, this project simulates the TeamViewer application. Once the connection is established,
 the client is granted full control of the server via mouse and keyboard. Meanwhile, the server
 continuously updates the screen for the client in real-time.

There are our team's infomations:
- 22120148: [Quang-Khai Le](https://github.com/john0148)
- 22120282: [Gia-Phuc Song-Dong](https://github.com/fusodoya)
- 22120333: [Quang-Thang Nguyen](https://github.com/thanguyen165)
  
## Video demo
[![image](https://github.com/user-attachments/assets/1273a230-3052-45d8-be23-97e1f372bb23)
](https://www.youtube.com/watch?v=l2N1-HuA4dM)

# How to Use MSYS2 to Run a Remote Desktop Project
## Note: Use MSYS2 MINGW64
![image-5](https://github.com/user-attachments/assets/10918bd6-c85f-4374-b38a-f609025ecb5d)


## BUILD INSTRUCTIONS

- Copy the ```lib``` folder and paste it into all 3 directories.
Commands to start the server:
- Start the MSYS2 software
- Navigate to the directory containing the makefile, Net folder, server folder, obj folder, and lib folder with the required libraries.
- Enter the command `make server` and press enter to build the server.
- Enter the command `./server.exe + port` to start the server and make it ready for connections.
  For example: `./server.exe 12345`

Commands to start the client:
- Start the MSYS2 software
- Navigate to the directory containing the makefile, Net folder, server folder, obj folder, bin folder, and lib folder with the required libraries.
- Enter the command `make` and press enter to build the client.
- Enter the command `./bin/client.exe` to start the client to connect to the machines.

## Here are the commands to install the libraries if you want to explore further. Please note that we have already included the necessary libraries for running the remote desktop in the lib folder.
- ### `pacman -Syu`: update all installed MSYS2 packages to the latest version

  - `-S`: option to install or update a package
  - `yu`: option to update all packages, including system and user-installed packages.

- ### `pacman -Su`: option to update all packages, including system packages.

- ### `pacman -S mingw-w64-x86_64-toolchain`

  - **mingw-w64-x86_64-toolchain**: provides the development tools to compile and run native C/C++ programs on Windows (prefer to use this over the next command).

- ### `pacman -S mingw-w64-x86_64-SDL2`
  - Used to download the SDL2 library.

- ### `pacman -S mingw-w64-x86_64-SDL2_image`
  - Used to download the SDL2_image library.

- ### `pacman -S mingw-w64-x86_64-opencv`
  - Used to download the opencv2 library.
