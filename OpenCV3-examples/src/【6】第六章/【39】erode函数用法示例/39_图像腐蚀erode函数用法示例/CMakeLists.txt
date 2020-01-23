add_executable(39_erode 39_erode.cpp)
target_link_libraries(39_erode ${OpenCV_LIBS})
add_custom_command(TARGET 39_erode
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
