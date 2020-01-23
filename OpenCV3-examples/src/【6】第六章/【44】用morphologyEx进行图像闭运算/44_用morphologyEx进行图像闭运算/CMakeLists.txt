add_executable(44_Closing 44_Closing.cpp)
target_link_libraries(44_Closing ${OpenCV_LIBS})
add_custom_command(TARGET 44_Closing
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
