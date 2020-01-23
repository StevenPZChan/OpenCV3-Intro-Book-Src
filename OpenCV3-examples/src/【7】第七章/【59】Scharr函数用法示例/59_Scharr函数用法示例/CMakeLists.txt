add_executable(59_Scharr 59_Scharr.cpp)
target_link_libraries(59_Scharr ${OpenCV_LIBS})
add_custom_command(TARGET 59_Scharr
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
