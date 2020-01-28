add_executable(90_SurfDescriptorExtractor 90_SurfDescriptorExtractor.cpp)
target_link_libraries(90_SurfDescriptorExtractor ${OpenCV_LIBS})
add_custom_command(TARGET 90_SurfDescriptorExtractor
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
