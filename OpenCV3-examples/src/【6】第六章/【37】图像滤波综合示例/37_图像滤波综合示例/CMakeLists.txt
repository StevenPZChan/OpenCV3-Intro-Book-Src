add_executable(37_ImageFiltering 37_ImageFiltering.cpp)
target_link_libraries(37_ImageFiltering ${OpenCV_LIBS})
add_custom_command(TARGET 37_ImageFiltering
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
