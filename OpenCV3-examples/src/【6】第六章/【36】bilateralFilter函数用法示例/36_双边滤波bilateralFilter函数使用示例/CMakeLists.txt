add_executable(36_bilateralFilter 36_bilateralFilter.cpp)
target_link_libraries(36_bilateralFilter ${OpenCV_LIBS})
add_custom_command(TARGET 36_bilateralFilter
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
