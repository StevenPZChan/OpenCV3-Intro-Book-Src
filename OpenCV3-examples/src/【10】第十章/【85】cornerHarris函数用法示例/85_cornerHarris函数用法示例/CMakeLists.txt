add_executable(85_cornerHarris 85_cornerHarris.cpp)
target_link_libraries(85_cornerHarris ${OpenCV_LIBS})
add_custom_command(TARGET 85_cornerHarris
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
