add_library(process
SHARED
process.cpp
)

target_include_directories(process
PUBLIC
${CMAKE_CURRENT_SOURCE_DIR} # 暴露 process.h 的路径
)

target_link_libraries(process
PUBLIC
pnc_map
)