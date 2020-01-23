add_executable(49_floodFill 49_floodFill.cpp)
target_link_libraries(49_floodFill ${OpenCV_LIBS})
add_custom_command(TARGET 49_floodFill
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
