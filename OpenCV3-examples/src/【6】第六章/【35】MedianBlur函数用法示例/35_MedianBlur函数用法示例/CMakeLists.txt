add_executable(35_medianBlur 35_medianBlur.cpp)
target_link_libraries(35_medianBlur ${OpenCV_LIBS})
add_custom_command(TARGET 35_medianBlur
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
