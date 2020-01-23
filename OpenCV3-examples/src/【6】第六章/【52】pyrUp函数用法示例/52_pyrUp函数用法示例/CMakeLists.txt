add_executable(52_pyrUp 52_pyrUp.cpp)
target_link_libraries(52_pyrUp ${OpenCV_LIBS})
add_custom_command(TARGET 52_pyrUp
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
