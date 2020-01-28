add_executable(95_OrbFeatureDetector 95_OrbFeatureDetector.cpp)
target_link_libraries(95_OrbFeatureDetector ${OpenCV_LIBS})
add_custom_command(TARGET 95_OrbFeatureDetector
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/1.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
