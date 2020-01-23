add_executable(31_boxFilter 31_boxFilter.cpp)
target_link_libraries(31_boxFilter ${OpenCV_LIBS})
add_custom_command(TARGET 31_boxFilter
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
