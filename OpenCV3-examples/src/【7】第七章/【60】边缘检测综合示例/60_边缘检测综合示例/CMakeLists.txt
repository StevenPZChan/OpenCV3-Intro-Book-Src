add_executable(60_EdgeDetection 60_EdgeDetection.cpp)
target_link_libraries(60_EdgeDetection ${OpenCV_LIBS})
add_custom_command(TARGET 60_EdgeDetection
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
