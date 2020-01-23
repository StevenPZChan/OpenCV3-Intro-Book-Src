add_executable(66_remap2 66_remap2.cpp)
target_link_libraries(66_remap2 ${OpenCV_LIBS})
add_custom_command(TARGET 66_remap2
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
