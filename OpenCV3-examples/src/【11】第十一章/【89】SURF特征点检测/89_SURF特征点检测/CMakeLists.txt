add_executable(89_SurfFeatureDetector 89_SurfFeatureDetector.cpp)
target_link_libraries(89_SurfFeatureDetector ${OpenCV_LIBS})
add_custom_command(TARGET 89_SurfFeatureDetector
        POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy_if_different ${CMAKE_CURRENT_SOURCE_DIR}/*.jpg ${EXECUTABLE_OUTPUT_PATH}
        )
