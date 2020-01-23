add_executable(2_ShowImage 2_ShowImage.cpp)
target_link_libraries(2_ShowImage ${OpenCV_LIBS})
add_custom_command(TARGET 2_ShowImage
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
