# 🧗 Interactive Climbing Wall Project

![C++](https://img.shields.io/badge/C++-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![Qt](https://img.shields.io/badge/Qt-41CD52?style=flat&logo=qt&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=opencv&logoColor=white)

An interactive climbing wall system that uses computer vision and motion tracking to create engaging games and training exercises for climbers. This project was developed as part of a 2nd-year university project (BUT Informatique) by a team of 4 students.

## 📖 Project Context

This was one of our first major software engineering projects during our second year of the University Technology Degree (BUT) in Computer Science. Working as a team of four, we built a complete interactive system combining hardware calibration, computer vision, and a user-friendly graphical interface to bring innovation to indoor climbing experiences.

The project demonstrates our learning in:
- **Object-oriented programming** with C++ and Qt framework
- **Computer vision** using Python, OpenCV, and MediaPipe
- **Design patterns** (MVC, Singleton, Observer)
- **Database management** with SQLite
- **Team collaboration** and version control

## 🎮 Features

### Games & Training Modes

1. **🎯 Climbing Routes (Parcours)**
   - Create custom climbing routes with color-coded holds
   - Track and store route completions
   - View personal and global leaderboards
   - Edit existing routes

2. **🏓 Pong Game**
   - Interactive Pong game controlled by body movements
   - Score tracking system
   - Real-time motion detection using MediaPipe

3. **🌀 Twister Mode**
   - Dynamic climbing challenge inspired by the classic Twister game
   - Reflex-based gameplay
   - Progressive difficulty system

### System Features

- **📹 Camera Calibration**: Precise calibration system using ChArUco boards for accurate tracking
- **👤 User Management**: Login system with user profiles and progress tracking
- **📊 Score Tracking**: Comprehensive scoring system across all game modes
- **🎨 Visual Interface**: Qt-based GUI with intuitive navigation
- **💾 Database Integration**: SQLite database for persistent storage of users, routes, and scores

## 🏗️ Architecture

The project follows a **Model-View-Controller (MVC)** architecture with additional design patterns:

- **Singleton Pattern**: Used for `DbManager` and `UserConnected` classes to ensure single instances
- **Observer Pattern**: Implemented for real-time updates between model and view
- **Abstract Controllers**: Modular control system for different game actions

### Key Components

```
├── GUI Layer (Qt Widgets)
│   ├── Main Menu
│   ├── Game Menus (Pong, Twister, Routes)
│   ├── Calibration Interface
│   └── Score Displays
│
├── Controllers (AbstractController)
│   ├── ControllerRemoveParcours
│   └── ControllerAddScore
│
├── Models
│   ├── DbManager (Database operations)
│   ├── Data (Calibration data)
│   ├── Prise (Climbing holds)
│   └── UserConnected (Session management)
│
└── Computer Vision (Python)
    ├── detectionMain.py (MediaPipe pose detection)
    ├── testCalibrage.py (Calibration testing)
    └── image_capture.py (Camera interface)
```

## 🛠️ Technologies Used

### C++ / Qt
- **Qt 5/6**: GUI framework for the main application
- **Qt Widgets**: Window management and UI components
- **Qt SQL**: Database integration
- **Pybind11**: Python-C++ binding for computer vision integration

### Python
- **OpenCV**: Image processing and camera calibration
- **MediaPipe**: Real-time pose detection and hand tracking
- **NumPy**: Numerical computations for coordinate processing

### Database
- **SQLite**: Lightweight database for storing users, routes, and scores

### Other
- **Boost**: Inter-process communication libraries
- **Visual Studio**: Development environment

## 🚀 Getting Started

### Prerequisites

- Visual Studio 2019 or later
- Qt 5.x or Qt 6.x
- Python 3.8+
- OpenCV
- MediaPipe
- Boost libraries
- Webcam for motion tracking

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Khrabehi/ClimbingProject.git
   cd ClimbingProject
   ```

2. **Install Python dependencies**
   ```bash
   pip install opencv-python mediapipe numpy
   ```

3. **Configure Qt in Visual Studio**
   - Install Qt VS Tools extension
   - Configure Qt version in Visual Studio settings

4. **Build the solution**
   - Open `testIHMClimingProject/testIHMClimingProject.sln`
   - Build the solution in Visual Studio

5. **Run calibration**
   - Launch the application
   - Go to Parameters → Calibration
   - Follow on-screen instructions to calibrate your camera

6. **Start playing!**
   - Create a user account
   - Select a game mode
   - Enjoy interactive climbing!

## 📸 Camera Calibration

The system uses ChArUco board calibration for precise tracking:

1. Print a ChArUco calibration board
2. Open the calibration menu in the application
3. Position the board in front of the camera
4. Capture calibration image
5. The system will compute camera matrix and distortion coefficients

## 💾 Database Schema

The SQLite database stores:
- **Users**: Username, password, statistics
- **Routes (Parcours)**: Route configurations, difficulty, holds positions
- **Scores**: User scores per game mode and route
- **Calibration Data**: Camera parameters and transformation matrices


## 👥 Team

This project was developed by a team of 4 students as part of our BUT Informatique curriculum.


**Note**: This was an early learning project, and the code may contain areas for improvement.
