add_executable(22_UseIteratorAccessPixel 22_UseIteratorAccessPixel.cpp)
target_link_libraries(22_UseIteratorAccessPixel ${OpenCV_LIBS})
add_custom_command(TARGET 22_UseIteratorAccessPixel
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
