add_executable(54_PyrAndResize 54_PyrAndResize.cpp)
target_link_libraries(54_PyrAndResize ${OpenCV_LIBS})
add_custom_command(TARGET 54_PyrAndResize
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
