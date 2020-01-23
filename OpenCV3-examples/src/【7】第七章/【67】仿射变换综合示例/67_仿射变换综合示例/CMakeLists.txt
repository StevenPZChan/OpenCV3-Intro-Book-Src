add_executable(67_AffineTransform 67_AffineTransform.cpp)
target_link_libraries(67_AffineTransform ${OpenCV_LIBS})
add_custom_command(TARGET 67_AffineTransform
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
