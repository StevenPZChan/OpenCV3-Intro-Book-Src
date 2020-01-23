add_executable(1_HelloOpenCV 1_HelloOpenCV.cpp)
target_link_libraries(1_HelloOpenCV ${OpenCV_LIBS})
add_custom_command(TARGET 1_HelloOpenCV
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
