# project
cmake_minimum_required (VERSION 2.8)
project (RenderingPlugin)
ADD_DEFINITIONS(-DUNITY_LINUX=1)

# use opencv to read and show img
find_package(OpenCV REQUIRED)
find_package( OpenGL REQUIRED )
find_package( GLEW REQUIRED )


include_directories(
${PROJECT_SOURCE_DIR}
${PROJECT_SOURCE_DIR}/Unity
${OPENCV_INCLUDE_DIRS}
${OPENGL_INCLUDE_DIR}
${GLEW_INCLUDE_DIR}
)
# use sse3 instruction set
#SET(CMAKE_CXX_FLAGS "-msse3")

set(SOURCE_FILES RenderingPlugin.cpp VideoCap.cpp)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/../UnityProject (copy)/Assets/Plugins/x86_64 )
add_library(RenderingPlugin SHARED ${SOURCE_FILES} )

