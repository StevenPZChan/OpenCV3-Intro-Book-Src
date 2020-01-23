add_executable(87_goodFeaturesToTrack 87_goodFeaturesToTrack.cpp)
target_link_libraries(87_goodFeaturesToTrack ${OpenCV_LIBS})
add_custom_command(TARGET 87_goodFeaturesToTrack
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
