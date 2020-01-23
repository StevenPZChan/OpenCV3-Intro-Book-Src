add_executable(27_ChangeContrastAndBright 27_ChangeContrastAndBright.cpp)
target_link_libraries(27_ChangeContrastAndBright ${OpenCV_LIBS})
add_custom_command(TARGET 27_ChangeContrastAndBright
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
