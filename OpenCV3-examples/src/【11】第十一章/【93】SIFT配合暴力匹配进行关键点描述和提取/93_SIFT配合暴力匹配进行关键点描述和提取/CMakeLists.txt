add_executable(93_SiftAndBFMatcher 93_SiftAndBFMatcher.cpp)
target_link_libraries(93_SiftAndBFMatcher ${OpenCV_LIBS})
add_custom_command(TARGET 93_SiftAndBFMatcher
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
