add_executable(91_FlannBasedMatcher 91_FlannBasedMatcher.cpp)
target_link_libraries(91_FlannBasedMatcher ${OpenCV_LIBS})
add_custom_command(TARGET 91_FlannBasedMatcher
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
