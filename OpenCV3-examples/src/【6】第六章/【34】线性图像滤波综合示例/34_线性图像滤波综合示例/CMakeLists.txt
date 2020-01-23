add_executable(34_LinearImageFilter 34_LinearImageFilter.cpp)
target_link_libraries(34_LinearImageFilter ${OpenCV_LIBS})
add_custom_command(TARGET 34_LinearImageFilter
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
