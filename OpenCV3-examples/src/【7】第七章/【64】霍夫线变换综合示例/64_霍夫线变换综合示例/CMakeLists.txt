add_executable(64_HoughLines 64_HoughLines.cpp)
target_link_libraries(64_HoughLines ${OpenCV_LIBS})
add_custom_command(TARGET 64_HoughLines
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
