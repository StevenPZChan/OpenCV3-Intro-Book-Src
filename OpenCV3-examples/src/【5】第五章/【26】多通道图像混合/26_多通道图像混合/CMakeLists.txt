add_executable(26_MultiChannelImageBlending 26_MultiChannelImageBlending.cpp)
target_link_libraries(26_MultiChannelImageBlending ${OpenCV_LIBS})
add_custom_command(TARGET 26_MultiChannelImageBlending
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
