project(new_lib)

file(GLOB_RECURSE SOURCES "src/*.cpp" "src/*.c" "include/*.h")

add_library(${PROJECT_NAME} STATIC ${SOURCES})
add_library(libs::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

target_include_directories(${PROJECT_NAME} INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
