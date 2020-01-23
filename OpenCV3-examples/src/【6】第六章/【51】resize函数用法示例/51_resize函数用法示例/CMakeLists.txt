add_executable(51_resize 51_resize.cpp)
target_link_libraries(51_resize ${OpenCV_LIBS})
add_custom_command(TARGET 51_resize
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
