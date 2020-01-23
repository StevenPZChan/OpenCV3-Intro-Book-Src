add_executable(72_convexHull2 72_convexHull2.cpp)
target_link_libraries(72_convexHull2 ${OpenCV_LIBS})
add_custom_command(TARGET 72_convexHull2
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
