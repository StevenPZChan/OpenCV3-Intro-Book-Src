add_executable(28_DFT 28_DFT.cpp)
target_link_libraries(28_DFT ${OpenCV_LIBS})
add_custom_command(TARGET 28_DFT
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
