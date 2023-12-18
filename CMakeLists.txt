cmake_minimum_required(VERSION 3.10)
project(RiceCookerProject)

# Locate GTest
find_package(GTest REQUIRED)

# Include headers
include_directories(include)

add_subdirectory(tests)

# Add the source files
set(SOURCE_FILES
    src/RiceCooker.cpp
    tests/RiceCookerTest.cpp
)

# Create the executable for your main program
add_executable(RiceCooker ${SOURCE_FILES})

# Create the executable for your tests
add_executable(RiceCookerTest tests/RiceCookerTest.cpp)

# Link against GTest and pthread library
target_link_libraries(RiceCookerTest GTest::GTest GTest::Main pthread)
