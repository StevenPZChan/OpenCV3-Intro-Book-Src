add_executable(43_Opening 43_Opening.cpp)
target_link_libraries(43_Opening ${OpenCV_LIBS})
add_custom_command(TARGET 43_Opening
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
