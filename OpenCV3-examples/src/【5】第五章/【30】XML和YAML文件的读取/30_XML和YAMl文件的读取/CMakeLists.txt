add_executable(30_Read_XML_and_YAML_File 30_Read_XML_and_YAML_File.cpp)
target_link_libraries(30_Read_XML_and_YAML_File ${OpenCV_LIBS})
add_custom_command(TARGET 30_Read_XML_and_YAML_File
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/test.yaml ${EXECUTABLE_OUTPUT_PATH}
        )
