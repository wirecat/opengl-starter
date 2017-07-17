cmake_minimum_required(VERSION 3.5)
project(ogl)

find_package(OpenGL REQUIRED)

include_directories(glad/include)

add_executable(main main.cpp glad/src/glad.c)

target_link_libraries(main GLEW glfw3 dl X11 Xrandr pthread Xinerama Xcursor)

#g++ main.cpp glad/src/glad.c -I glad/include/ -ldl -lGLEW -lglfw3 -lX11 -lXrandr -lpthread -lXinerama -lXcursor
