add_executable(11_ObjectDetection 11_ObjectDetection.cpp)
target_link_libraries(11_ObjectDetection ${OpenCV_LIBS})
add_custom_command(TARGET 11_ObjectDetection
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.xml ${EXECUTABLE_OUTPUT_PATH}
        )
