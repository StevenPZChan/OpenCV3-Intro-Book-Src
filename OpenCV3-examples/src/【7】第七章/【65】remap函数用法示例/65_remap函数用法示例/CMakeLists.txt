add_executable(65_remap 65_remap.cpp)
target_link_libraries(65_remap ${OpenCV_LIBS})
add_custom_command(TARGET 65_remap
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
