# Astro Clash

## A Retro Arcade Game in C++ & Qt/QML

Astro Clash is a retro arcade-style game built using **Qt C++ and QML**, designed to teach beginning developers fundamentals step-by-step. Dodge enemies, fire bullets, and enjoy real-time pixel action while learning how to build a full game using C++ backend and QML frontend.

## How to use Astro Clash

You can clone and build the project locally to play the complete game and explore the codebase.

```bash
git clone https://github.com/kaustuvpokharel/Astro-Clash.git
cd Astro-Clash
```

## How to install Astro Clash

### Prerequisites

You will need Qt 6.2+ installed with Qt Creator, ensuring that Qt Quick and CMake components are included in your installation.

### Build Instructions

Navigate to your project directory and build using CMake:

```bash
mkdir build
cd build
cmake ..
make
```

### Running the Game

After successful build, execute the game:

```bash
./play
```

## Game Features

Astro Clash includes the following gameplay elements:

| Feature | Description |
|---------|-------------|
| **Rocket Control** | Thrust-based movement system with realistic physics |
| **Enemy System** | Multiple enemy types with random spawning patterns |
| **Combat System** | Bullet firing with collision detection |
| **Visual Effects** | Blast animations on enemy destruction |
| **UI Elements** | Game over overlay with restart and close options |
| **Scoring** | Real-time score tracking system |

## Project Structure

The codebase is organized into the following structure:

```
├── CMakeLists.txt                 # Build configuration
├── README.md                      # Project documentation
├── assets/                        # Graphics and font resources
│   ├── Doto-Bold.ttf             # Bold font variant
│   ├── Doto-ExtraBold.ttf        # Extra bold font variant
│   ├── asset.qrc & assets.qrc    # Qt resource files
│   ├── bullet.png                # Bullet sprite
│   ├── enemy1-5.png              # Enemy sprite variants
│   ├── rocket.png                # Player rocket sprite
│   └── thruster.gif              # Rocket thruster animation
├── build/                         # Build output directory
├── qml/                          # QML frontend components
│   ├── Enemy.qml                 # Enemy visual component
│   ├── bullet.qml                # Bullet visual component
│   ├── bullet.qrc                # QML resource file
│   └── main.qml                  # Main game interface
└── src/                          # C++ backend source files
    ├── Bullet.cpp/h              # Bullet logic implementation
    ├── Controller.cpp/h          # Main game controller
    ├── Enemy.cpp/h               # Enemy behavior logic
    └── main.cpp                  # Application entry point
```

## Technical Implementation

### Core Technologies

| Layer | Technology |
|-------|------------|
| **Frontend** | Qt Quick / QML |
| **Backend** | Qt C++ (QObject) |
| **Build System** | CMake |
| **Assets** | Pixel art PNG/GIF |
| **Animations** | AnimatedImage with custom logic |

### Key Programming Concepts

The project demonstrates several important programming concepts:

- **QQmlListProperty<T> usage** for dynamic QML list binding
- **QTimer handling** for 60FPS game loop updates
- **Game loop architecture** implemented in C++
- **Interactive QML overlays** for user interface
- **Keyboard input handling** within QML components
- **C++ and QML integration** for real-time game programming

## Screenshots

> W.I.P

## More Information about Astro Clash

For additional documentation or to contribute to the project, visit the project repository. The game serves as an excellent introduction to Qt development and game programming concepts for developers of all skill levels.
