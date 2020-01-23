add_executable(86_cornerHarris 86_cornerHarris.cpp)
target_link_libraries(86_cornerHarris ${OpenCV_LIBS})
add_custom_command(TARGET 86_cornerHarris
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
