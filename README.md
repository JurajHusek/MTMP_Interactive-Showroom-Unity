# Pirate Ship Showroom – Unity Interactive Visualization  
### Assignment 3 + Bonus Features (MTMP – Multimedia, FEI STU)

This project is an interactive 3D showroom visualization of two pirate ships created in Unity.  
The user can display the ships, read information panels, rotate objects, switch between multiple viewpoints, or activate a free-camera exploration mode.  
An automatic showroom mode is also included, showcasing both ships with timed transitions and animations.

This project was created as the solution for **Assignment 3 of the MTMP course** at FEI STU.  
A full written documentation is included in:  
**dokumentacia_Z3_UNITY_BONUS_Husek.pdf**

Runnable build is located in **Build_Z3_UNITY_BONUS_Husek.rar**

---

# Features Overview

## Core Features
- **Two pirate ships**, each with its own information panels and camera viewpoints.
- **Manual showroom mode** – the player controls the camera and interactions.
- **Automatic showroom mode** – hands-free presentation with timed steps.
- **Unlocked Camera mode** – free cam movement similar to Unity Scene View.
- **Ship interactions** – rotate ships, toggle flags, adjust sails.
- **UI navigation** – switch ships, switch view presets, show/hide info panels.

---

# Controls

## Unlocked Camera Mode

| Action | Control |
|--------|----------|
| Move camera | WASD / arrow keys |
| Move upward | Spacebar |
| Vertical pan | Left mouse drag |
| Camera rotation | Right mouse drag |
| Zoom | Scroll wheel / `+` / `-` |

Camera controls implemented in **CameraController.cs**
---

# Manual Showroom

Includes:

1. **Switching between multiple predefined viewpoints** per ship.
2. **Start/Stop ship rotation** (play/pause buttons) – powered by `UiManager`.
3. **Unlocked Camera toggle**, enabling free exploration.
4. **Ship detail controls** – hide/show flags, tighten sails, etc.
5. **Switching between ships** using left/right UI arrows.

UI and rotation logic is handled in **UiManager.cs**
Camera and movement logic is handled in **CameraController.cs**

---

# Automatic Showroom

Automated logic is implemented in **ShowroomManager.cs** 

### Automatic mode includes:
- Automatic transitions through all camera targets.
- Displaying information panels per target.
- Triggering timed animations (e.g., ship rotation).
- Delay system for each step of the sequence.
- Return to main menu after finishing the full cycle.
- Force stop button.

---

# Script Overview

## CameraController.cs  
- Smooth free-cam movement  
- Smooth zoom with clamping  
- LMB vertical dragging  
- Smooth transitions to specific targets (MoveToTarget)  
- Smooth camera lock/unlock logic  
- Automatic camera moves during presentation  
- UI indicator for lock/unlock state  

---

## UiManager.cs  
- Independent rotation control for both ships  
- Toggle for sails, flags, and UI elements  
- Lightweight start/stop rotation logic ideal for UI buttons  

---

## ShowroomManager.cs  
- Automatic timed sequence of camera targets  
- Controls which info panel is visible  
- Starts/stops ship rotation at specific steps  
- Handles menu transitions and exit logic  
- Automatically returns to main menu after autoplay  

---

# Unity Assets Used

As listed in the official documentation **dokumentacia_Z3_UNITY_BONUS_Husek.pdf**

- **POLYGON – Pirate Pack (Synty)**  
- **Cloth Animation Based Flag (deprecated)**  
- **Legacy Image Effects (deprecated)**  
- **Clean Vector Icons**  
- **Simple Fantasy GUI**  
- **FC Pirate Music Pack**

---

# How to Run Build
1. Extract Build_Z3_UNITY_BONUS_Husek.rar
2. Launch Pirate Ship Showroom - Juraj Husek.exe

# How to open project
1. Open the Unity project (recommended Unity 2021.3+).
2. Import third-party assets according to documentation **dokumentacia_Z3_UNITY_BONUS_Husek.pdf**
3. Open the scene:  
/Scenes/showroom.unity
4. Press **Play**.
5. Choose from:
- **Manual Showroom**
- **Automatic Showroom**
- **Info Panel**

---

# Bonus Features Implemented

- Full **automatic presentation system**  
- **Ship rotation** system with UI toggles  
- **Unlocked free camera mode**  
- **Multiple view presets** per ship  
- **UI animations**  
- **Detail toggles** (flags, sails…)  

---


# License

This project is intended for academic use for MTMP (Multimedia) at FEI STU.

---

# Author

**Bc. Juraj Hušek (2025)**  
Faculty of Electrical Engineering and Informatics  
Slovak University of Technology in Bratislava
