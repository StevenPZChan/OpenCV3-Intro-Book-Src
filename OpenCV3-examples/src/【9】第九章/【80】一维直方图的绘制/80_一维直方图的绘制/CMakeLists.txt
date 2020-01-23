add_executable(80_Histogram2 80_Histogram2.cpp)
target_link_libraries(80_Histogram2 ${OpenCV_LIBS})
add_custom_command(TARGET 80_Histogram2
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
