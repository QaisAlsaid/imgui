cmake_minimum_required(VERSION 3.28)
project(imgui)
include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/backends
    ${CMAKE_CURRENT_SOURCE_DIR}/
    ${CMAKE_CURRENT_SOURCE_DIR}/../glfw/include)
set(IMGUI_SRC imconfig.h imgui.cpp imgui.h
    imgui_demo.cpp imgui_draw.cpp
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_glfw.h imgui_internal.h
    imgui_tables.cpp imgui_widgets.cpp
    imstb_rectpack.h imstb_textedit.h
    backends/imgui_impl_opengl3.h
    imstb_truetype.h
    backends/imgui_impl_opengl3.cpp)
add_library(imgui STATIC ${IMGUI_SRC})
#target_compile_definitions(${PROJECT_NAME} PUBLIC IMGUI_IMPL_OPENGL_LOADER_GLAD)
