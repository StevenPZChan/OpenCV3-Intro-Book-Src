add_executable(78_inpaint 78_inpaint.cpp)
target_link_libraries(78_inpaint ${OpenCV_LIBS})
add_custom_command(TARGET 78_inpaint
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
