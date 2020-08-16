project(new_app)

set(CMAKE_CXX_STANDARD 14)

file(GLOB_RECURSE SOURCES "src/*.cpp" "src/*.c" "include/*.h")

add_executable(${PROJECT_NAME} ${SOURCES})

target_link_libraries(${PROJECT_NAME}
        PRIVATE
        libs::new_lib
        )
