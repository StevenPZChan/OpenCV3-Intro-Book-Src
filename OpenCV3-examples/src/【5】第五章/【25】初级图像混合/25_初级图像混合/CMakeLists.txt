add_executable(25_ImageBlending 25_ImageBlending.cpp)
target_link_libraries(25_ImageBlending ${OpenCV_LIBS})
add_custom_command(TARGET 25_ImageBlending
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
