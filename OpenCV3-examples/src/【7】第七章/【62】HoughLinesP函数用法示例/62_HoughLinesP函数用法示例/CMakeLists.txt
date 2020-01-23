add_executable(62_HoughLinesP 62_HoughLinesP.cpp)
target_link_libraries(62_HoughLinesP ${OpenCV_LIBS})
add_custom_command(TARGET 62_HoughLinesP
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
