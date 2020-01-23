add_executable(68_equalizeHist 68_equalizeHist.cpp)
target_link_libraries(68_equalizeHist ${OpenCV_LIBS})
add_custom_command(TARGET 68_equalizeHist
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
