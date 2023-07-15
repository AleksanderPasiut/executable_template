cmake_minimum_required(VERSION 3.10)
project(executable_template)

add_executable(${PROJECT_NAME} src/main.cpp)

add_dependencies(${PROJECT_NAME} library_template)
add_subdirectory(src/library_template)

target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_SOURCE_DIR})
target_link_libraries(${PROJECT_NAME} PRIVATE -lstdc++)

link_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_BINARY_DIR}/src/library_template)
target_link_libraries(${PROJECT_NAME} PRIVATE library_template)

