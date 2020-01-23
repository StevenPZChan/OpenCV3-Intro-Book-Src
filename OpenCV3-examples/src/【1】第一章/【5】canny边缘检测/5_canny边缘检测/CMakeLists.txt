add_executable(5_Canny 5_Canny.cpp)
target_link_libraries(5_Canny ${OpenCV_LIBS})
add_custom_command(TARGET 5_Canny
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
