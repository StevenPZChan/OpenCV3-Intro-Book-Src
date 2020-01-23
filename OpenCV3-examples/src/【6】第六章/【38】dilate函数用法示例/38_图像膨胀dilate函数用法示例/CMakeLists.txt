add_executable(38_dilate 38_dilate.cpp)
target_link_libraries(38_dilate ${OpenCV_LIBS})
add_custom_command(TARGET 38_dilate
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
