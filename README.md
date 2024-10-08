# Voxall

Voxall is a voxel editor and game engine. It allows users to create, import, edit, and save `.vox` files, as well as develop full standalone voxel-based games.

## Features

- **Editor Mode**:
    - Orbit view: Middle mouse button + mouse move
    - Pan view: Left Shift + Middle mouse button + mouse move
    - Zoom: Scroll wheel
    - Add voxel: Left click
    - Remove voxel: Right click

- **Play Mode**:
    - Movement: WASD + Space bar + Left Ctrl + Mouse movement
    - Add voxel: Left click
    - Remove voxel: Right click
    - Cursor locked to the center of the screen

- **Rendering**:
    - Displays a lit cube
    - Supports textures with a fallback color

## Future Plans

- Toolbar for saving, exiting, importing `.vox` files, etc.
- UI for voxel color selection and other tools
- Chunking for map generation
- Height maps for voxel terrains
- Configuration file for various settings

## Installation

### Prerequisites

- CMake 3.29 or newer
- vcpkg
- CLion 2024.2.1
- C++20 or newer

### Setup

1. **Clone the repository**:
    ```sh
    git clone https://github.com/yourusername/Voxall.git
    cd Voxall
    ```

2. **Install dependencies using vcpkg**:
    ```sh
    ./vcpkg install glfw3 glad glm
    ```

3. **Open the project in CLion**:
    - Open CLion and select `Open` from the welcome screen.
    - Navigate to the `Voxall` directory and open it.

4. **Configure CMake**:
    - Ensure that `CMakeLists.txt` is configured to use the vcpkg toolchain file:
      ```cmake
      if(DEFINED ENV{VCPKG_ROOT} AND NOT DEFINED CMAKE_TOOLCHAIN_FILE)
          set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake" CACHE STRING "")
      endif()
      ```

5. **Build the project**:
    - In CLion, click on the `Build` menu and select `Build Project`.

## Usage

- **Run the application**:
    - In CLion, click on the `Run` menu and select `Run 'Voxall'`.

- **Editor Mode**:
    - Use the middle mouse button to orbit the view.
    - Hold Left Shift and use the middle mouse button to pan the view.
    - Use the scroll wheel to zoom in and out.
    - Left click to add a voxel.
    - Right click to remove a voxel.

- **Play Mode**:
    - Press Left Shift + Tab to switch to play mode.
    - Use WASD for movement, Space bar to jump, Left Ctrl to crouch, and mouse movement to look around.
    - Left click to add a voxel.
    - Right click to remove a voxel.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any changes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.