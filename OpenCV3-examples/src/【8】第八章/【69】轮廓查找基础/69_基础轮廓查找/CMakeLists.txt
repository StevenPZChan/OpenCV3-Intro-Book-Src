add_executable(69_findContours 69_findContours.cpp)
target_link_libraries(69_findContours ${OpenCV_LIBS})
add_custom_command(TARGET 69_findContours
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
