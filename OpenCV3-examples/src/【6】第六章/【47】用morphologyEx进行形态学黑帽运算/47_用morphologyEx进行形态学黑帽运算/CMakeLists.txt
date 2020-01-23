add_executable(47_BlackHat 47_BlackHat.cpp)
target_link_libraries(47_BlackHat ${OpenCV_LIBS})
add_custom_command(TARGET 47_BlackHat
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
