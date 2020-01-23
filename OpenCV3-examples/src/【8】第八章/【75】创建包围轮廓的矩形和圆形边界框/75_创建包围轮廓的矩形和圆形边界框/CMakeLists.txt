add_executable(75_approxPolyDP 75_approxPolyDP.cpp)
target_link_libraries(75_approxPolyDP ${OpenCV_LIBS})
add_custom_command(TARGET 75_approxPolyDP
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
