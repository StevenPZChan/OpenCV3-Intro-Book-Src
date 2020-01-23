add_executable(55_threshold 55_threshold.cpp)
target_link_libraries(55_threshold ${OpenCV_LIBS})
add_custom_command(TARGET 55_threshold
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
