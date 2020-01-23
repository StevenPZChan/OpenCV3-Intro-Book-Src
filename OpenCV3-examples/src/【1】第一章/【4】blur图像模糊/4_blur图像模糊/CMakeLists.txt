add_executable(4_BlurImage 4_BlurImage.cpp)
target_link_libraries(4_BlurImage ${OpenCV_LIBS})
add_custom_command(TARGET 4_BlurImage
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
