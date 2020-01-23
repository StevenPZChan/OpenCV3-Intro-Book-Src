add_executable(17_CreateTrackbar 17_CreateTrackbar.cpp)
target_link_libraries(17_CreateTrackbar ${OpenCV_LIBS})
add_custom_command(TARGET 17_CreateTrackbar
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
