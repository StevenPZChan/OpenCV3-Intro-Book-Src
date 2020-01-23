add_executable(33_GaussianBlur 33_GaussianBlur.cpp)
target_link_libraries(33_GaussianBlur ${OpenCV_LIBS})
add_custom_command(TARGET 33_GaussianBlur
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
