add_executable(57_sobel 57_sobel.cpp)
target_link_libraries(57_sobel ${OpenCV_LIBS})
add_custom_command(TARGET 57_sobel
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
