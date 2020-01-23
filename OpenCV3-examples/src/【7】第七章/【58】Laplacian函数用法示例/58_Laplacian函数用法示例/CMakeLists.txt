add_executable(58_Laplacian 58_Laplacian.cpp)
target_link_libraries(58_Laplacian ${OpenCV_LIBS})
add_custom_command(TARGET 58_Laplacian
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
