cmake_minimum_required(VERSION 3.13)

project(
    hello 
    VERSION 0.0.1 
    LANGUAGES C CXX ASM
)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

add_subdirectory(greetings)

add_executable(
    ${PROJECT_NAME} 
    main.cpp
)

target_link_libraries(
    ${PROJECT_NAME} 
    greetings
)
