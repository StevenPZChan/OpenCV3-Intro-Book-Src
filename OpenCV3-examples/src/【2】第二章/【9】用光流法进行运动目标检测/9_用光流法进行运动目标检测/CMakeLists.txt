add_executable(9_OpticalFlow 9_OpticalFlow.cpp)
target_link_libraries(9_OpticalFlow ${OpenCV_LIBS})
add_custom_command(TARGET 9_OpticalFlow
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.avi ${EXECUTABLE_OUTPUT_PATH}
        )
