cmake_minimum_required(VERSION 3.17)
project(learn1)

set(CMAKE_CXX_STANDARD 14)

# 添加头文件
set(GLFW_H /usr/local/Cellar/glfw/3.3.2/include/GLFW)
set(GLAD_H /usr/local/include/glad)
include_directories(${GLFW_H} ${GLAD_H})

# 添加目标链接

set(GLFW_LINK /usr/local/Cellar/glfw/3.3.2/lib/libglfw.3.dylib)
link_libraries(${OPENGL} ${GLFW_LINK})

link_libraries(/usr/local/lib)
include_directories(/usr/local/include)
add_executable(learn1 main.cpp glad.c shader.h stb_image.h camera.h)
if (APPLE)
    target_link_libraries(learn1 "-framework OpenGL")
    target_link_libraries(learn1 "-framework GLUT")
endif()