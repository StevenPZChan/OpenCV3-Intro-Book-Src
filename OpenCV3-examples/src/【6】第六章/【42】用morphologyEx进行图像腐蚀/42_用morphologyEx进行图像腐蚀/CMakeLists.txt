add_executable(42_ErodeEX 42_ErodeEX.cpp)
target_link_libraries(42_ErodeEX ${OpenCV_LIBS})
add_custom_command(TARGET 42_ErodeEX
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
