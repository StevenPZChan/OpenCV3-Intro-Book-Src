add_executable(40_dilate_And_erode 40_dilate_And_erode.cpp)
target_link_libraries(40_dilate_And_erode ${OpenCV_LIBS})
add_custom_command(TARGET 40_dilate_And_erode
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
