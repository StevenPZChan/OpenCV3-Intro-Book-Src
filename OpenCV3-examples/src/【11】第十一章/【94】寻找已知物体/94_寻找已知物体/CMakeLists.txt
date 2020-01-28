add_executable(94_FindObject 94_FindObject.cpp)
target_link_libraries(94_FindObject ${OpenCV_LIBS})
add_custom_command(TARGET 94_FindObject
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
