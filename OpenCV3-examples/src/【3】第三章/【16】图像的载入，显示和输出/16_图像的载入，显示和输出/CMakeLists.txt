add_executable(16_LoadShowOutputImage 16_LoadShowOutputImage.cpp)
target_link_libraries(16_LoadShowOutputImage ${OpenCV_LIBS})
add_custom_command(TARGET 16_LoadShowOutputImage
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
