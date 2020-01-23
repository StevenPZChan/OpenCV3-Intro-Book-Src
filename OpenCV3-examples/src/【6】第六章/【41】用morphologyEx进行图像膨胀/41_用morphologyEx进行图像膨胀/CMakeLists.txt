add_executable(41_DilationEX 41_DilationEX.cpp)
target_link_libraries(41_DilationEX ${OpenCV_LIBS})
add_custom_command(TARGET 41_DilationEX
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
