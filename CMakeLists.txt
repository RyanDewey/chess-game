cmake_minimum_required(VERSION 3.14)

# Set your project name
project(HelloSFML)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find the SFML package
set(SFML_DIR "/opt/homebrew/Cellar/sfml/2.6.1/lib/cmake/SFML")
find_package(SFML 2.5 COMPONENTS system window graphics network audio REQUIRED)

# Add your source files
add_executable(HelloSFML main.cpp
        Connector.h)

# Link the SFML libraries to your executable
target_link_libraries(HelloSFML sfml-system sfml-window sfml-graphics sfml-network sfml-audio)
