add_executable(88_cornerSubPix 88_cornerSubPix.cpp)
target_link_libraries(88_cornerSubPix ${OpenCV_LIBS})
add_custom_command(TARGET 88_cornerSubPix
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
