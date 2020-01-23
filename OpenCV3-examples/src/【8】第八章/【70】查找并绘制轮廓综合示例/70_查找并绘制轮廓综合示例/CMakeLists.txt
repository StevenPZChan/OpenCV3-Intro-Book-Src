add_executable(70_FindAndDrawContours 70_FindAndDrawContours.cpp)
target_link_libraries(70_FindAndDrawContours ${OpenCV_LIBS})
add_custom_command(TARGET 70_FindAndDrawContours
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
