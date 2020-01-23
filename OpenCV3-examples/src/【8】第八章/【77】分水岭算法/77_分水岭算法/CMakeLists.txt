add_executable(77_watershed 77_watershed.cpp)
target_link_libraries(77_watershed ${OpenCV_LIBS})
add_custom_command(TARGET 77_watershed
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
