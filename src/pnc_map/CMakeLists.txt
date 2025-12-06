add_library(pnc_map
SHARED
pnc_map.cpp
)

# 暴露头文件路径：对外部可见，供 process 使用
target_include_directories(pnc_map
    PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR} # 暴露 pnc_map.h 的路径
)