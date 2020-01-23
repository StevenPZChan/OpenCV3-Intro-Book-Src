add_executable(82_compareHist 82_compareHist.cpp)
target_link_libraries(82_compareHist ${OpenCV_LIBS})
add_custom_command(TARGET 82_compareHist
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
