add_executable(63_HoughCircles 63_HoughCircles.cpp)
target_link_libraries(63_HoughCircles ${OpenCV_LIBS})
add_custom_command(TARGET 63_HoughCircles
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
