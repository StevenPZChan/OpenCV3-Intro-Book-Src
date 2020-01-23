add_executable(50_floodFill2 50_floodFill2.cpp)
target_link_libraries(50_floodFill2 ${OpenCV_LIBS})
add_custom_command(TARGET 50_floodFill2
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
