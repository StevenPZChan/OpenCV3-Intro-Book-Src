add_executable(3_ImageErode 3_ImageErode.cpp)
target_link_libraries(3_ImageErode ${OpenCV_LIBS})
add_custom_command(TARGET 3_ImageErode
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
