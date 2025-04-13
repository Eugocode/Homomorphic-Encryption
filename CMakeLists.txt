cmake_minimum_required(VERSION 3.15)
project(SimpleAdd)

# Tell CMake to use C++17 and Ninja
set(CMAKE_CXX_STANDARD 17)

# Find the OpenFHE library (adjust this path if needed)
find_package(OpenFHE REQUIRED)

# Add your source file
add_executable(simple-add src/simple-add.cpp)

# Link OpenFHE
target_link_libraries(simple-add OpenFHE::pke)