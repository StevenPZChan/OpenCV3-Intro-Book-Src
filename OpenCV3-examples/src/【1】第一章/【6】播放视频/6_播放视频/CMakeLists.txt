add_executable(6_PlayVideo 6_PlayVideo.cpp)
target_link_libraries(6_PlayVideo ${OpenCV_LIBS})
add_custom_command(TARGET 6_PlayVideo
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.avi ${EXECUTABLE_OUTPUT_PATH}
        )
