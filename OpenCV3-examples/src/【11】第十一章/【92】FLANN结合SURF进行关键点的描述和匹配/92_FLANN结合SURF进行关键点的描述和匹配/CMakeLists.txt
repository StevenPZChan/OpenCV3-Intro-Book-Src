add_executable(92_FLANN_and_SURF 92_FLANN_and_SURF.cpp)
target_link_libraries(92_FLANN_and_SURF ${OpenCV_LIBS})
add_custom_command(TARGET 92_FLANN_and_SURF
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
