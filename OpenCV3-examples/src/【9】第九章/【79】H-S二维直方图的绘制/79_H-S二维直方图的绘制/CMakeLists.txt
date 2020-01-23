add_executable(79_H-S-Histogram 79_H-S-Histogram.cpp)
target_link_libraries(79_H-S-Histogram ${OpenCV_LIBS})
add_custom_command(TARGET 79_H-S-Histogram
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
