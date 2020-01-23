add_executable(23_UseAtAccessPixel 23_UseAtAccessPixel.cpp)
target_link_libraries(23_UseAtAccessPixel ${OpenCV_LIBS})
add_custom_command(TARGET 23_UseAtAccessPixel
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
