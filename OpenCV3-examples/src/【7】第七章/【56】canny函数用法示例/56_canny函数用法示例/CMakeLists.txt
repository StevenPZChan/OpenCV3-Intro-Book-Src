add_executable(56_canny 56_canny.cpp)
target_link_libraries(56_canny ${OpenCV_LIBS})
add_custom_command(TARGET 56_canny
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
