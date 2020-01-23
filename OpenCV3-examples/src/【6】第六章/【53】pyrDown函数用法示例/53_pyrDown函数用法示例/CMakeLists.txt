add_executable(53_pyrDown 53_pyrDown.cpp)
target_link_libraries(53_pyrDown ${OpenCV_LIBS})
add_custom_command(TARGET 53_pyrDown
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
