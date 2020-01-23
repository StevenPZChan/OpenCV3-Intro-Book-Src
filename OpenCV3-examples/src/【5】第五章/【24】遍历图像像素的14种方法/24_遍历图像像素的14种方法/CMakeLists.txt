add_executable(24_14WaysToAccessPixel 24_14WaysToAccessPixel.cpp)
target_link_libraries(24_14WaysToAccessPixel ${OpenCV_LIBS})
add_custom_command(TARGET 24_14WaysToAccessPixel
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.png ${EXECUTABLE_OUTPUT_PATH}
        )
