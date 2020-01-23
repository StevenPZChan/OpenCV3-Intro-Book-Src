add_executable(32_blur 32_blur.cpp)
target_link_libraries(32_blur ${OpenCV_LIBS})
add_custom_command(TARGET 32_blur
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
