add_executable(83_calcBackProject 83_calcBackProject.cpp)
target_link_libraries(83_calcBackProject ${OpenCV_LIBS})
add_custom_command(TARGET 83_calcBackProject
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
