add_executable(76_ContourMoment 76_ContourMoment.cpp)
target_link_libraries(76_ContourMoment ${OpenCV_LIBS})
add_custom_command(TARGET 76_ContourMoment
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
