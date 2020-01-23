add_executable(46_TopHat 46_TopHat.cpp)
target_link_libraries(46_TopHat ${OpenCV_LIBS})
add_custom_command(TARGET 46_TopHat
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
