add_executable(84_matchTemplate 84_matchTemplate.cpp)
target_link_libraries(84_matchTemplate ${OpenCV_LIBS})
add_custom_command(TARGET 84_matchTemplate
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
