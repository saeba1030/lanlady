cmake_minimum_required(VERSION 3.20)
project(LanLady VERSION 0.1)

set(CMAKE_C_STANDARD 11)

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build)

file(GLOB_RECURSE SRC_FILES
    "src/*.c"
)

add_executable(${PROJECT_NAME}
    ${SRC_FILES}
)

# Predefines for compilers, check tasks.json
target_compile_definitions(${PROJECT_NAME} PUBLIC _DEBUG _UNICODE UNICODE)