# C GIF Maker 🎬

## Overview
This repository contains a command-line driven GIF/Movie Maker application written entirely in C. Developed as the final project for the Magshimim "Intro to C" course, this tool allows users to stitch together individual image frames to create, edit, save, and play custom animations. 

The project heavily utilizes **Singly Linked Lists** as its core data structure to manage frames dynamically, and integrates the **Raylib** graphics library to handle image rendering, timing, and visual effects.

## Features
### 🎞️ Core Frame Management
* **Add/Remove Frames:** Dynamically allocate and insert new frames (containing an image path, duration, and unique name) or remove existing ones.
* **Reorder Frames:** Change the sequence of the animation by moving frames to different indices within the linked list.
* **Timing Control:** Adjust the display duration (in milliseconds) of an individual frame or bulk-update the duration for all frames.

### 💾 Project Persistence
* **Save & Load:** Export your current GIF timeline to a custom text-based file format. The application accurately parses the saved files to reconstruct the linked list, allowing you to pause your work and resume later.

### 🎨 Image Filters & Rendering (Bonus Implemented!)
* **Raylib Playback:** Opens a dedicated graphics window to render the sequence of frames at their specified durations.
* **Custom Filters:** Apply visual effects to either a specific frame or the entire animation using Raylib's image manipulation tools:
    * Black & White (Grayscale)
    * Gaussian Blur (with adjustable strength)
    * Color Tinting (Red, Green, Blue, Yellow, Brown)

## Technical Architecture
* **Language:** C
* **Graphics/UI Library:** [Raylib](https://www.raylib.com/)
* **Core Data Structure:** Singly Linked List (`FrameNode` containing `Frame` structs).
* **Memory Management:** Extensive use of `malloc`, `calloc`, `realloc`, and `free` to safely manage string paths, names, and dynamic nodes without memory leaks.
* **Modularity:** Cleanly separated header (`.h`) and source (`.c`) files for linked list logic, file management, helper functions, and the Raylib view.

## How to Run
1. Ensure you have a C compiler (like GCC) and the **Raylib** library installed and configured on your system.
2. Compile the source files together. *(Example: `gcc *.c -o gifmaker.exe -lraylib -lgdi32 -lwinmm`)*
3. Run the executable.
4. Use the interactive terminal menu to create a new project or load an existing one, add paths to your local images, and start building your GIF!

## Disclaimer
This project was developed for educational purposes to demonstrate proficiency in C programming, pointer arithmetic, memory management, and data structures.
