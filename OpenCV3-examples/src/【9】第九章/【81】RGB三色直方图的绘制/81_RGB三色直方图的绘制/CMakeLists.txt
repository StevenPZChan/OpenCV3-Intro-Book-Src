add_executable(81_histogram3 81_histogram3.cpp)
target_link_libraries(81_histogram3 ${OpenCV_LIBS})
add_custom_command(TARGET 81_histogram3
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
