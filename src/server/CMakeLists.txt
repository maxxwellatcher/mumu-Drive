# 设置CMake的最低版本要求
cmake_minimum_required(VERSION 3.10)

# 设置项目名称和版本
project(server VERSION 1.0)

# 设置C++标准
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# 包含头文件目录
include_directories(${PROJECT_SOURCE_DIR}/include)

# 添加可执行文件
file(GLOB SOURCES "src/*.cc")

add_executable(server ${SOURCES})

# 如果有测试文件，可以添加测试可执行文件
# add_executable(test_my_project tests/test_my_class.cpp src/my_class.cpp)

# 启用测试
# enable_testing()
# add_test(NAME test_my_project COMMAND test_my_project)

# 如果有第三方库，可以在这里添加
# find_package(SomeLibrary REQUIRED)
# target_link_libraries(my_project SomeLibrary::SomeLibrary)

# 设置输出目录
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)