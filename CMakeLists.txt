cmake_minimum_required(VERSION 3.30.0)
project(planning
  VERSION 0.0.1
  DESCRIPTION "a demo of cmake planning"
  HOMEPAGE_URL "https://github.com/superdragonman/make_planning_demo"
  LANGUAGES CXX
  )

set(CMAKE_CXX_STANDARD 20)

set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin) 

add_subdirectory(src/pnc_map)
add_subdirectory(src/process)

add_executable(planning_main src/planning_main.cpp)

target_link_libraries(planning_main 
    PRIVATE 
    process 
)