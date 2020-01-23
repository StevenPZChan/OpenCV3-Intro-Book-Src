add_executable(21_UsePointerAccessPixel 21_UsePointerAccessPixel.cpp)
target_link_libraries(21_UsePointerAccessPixel ${OpenCV_LIBS})
add_custom_command(TARGET 21_UsePointerAccessPixel
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
