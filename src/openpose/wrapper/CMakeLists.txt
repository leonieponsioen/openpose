set(SOURCES
    defineTemplates.cpp
    wrapperStructFace.cpp
    wrapperStructHand.cpp
    wrapperStructInput.cpp
    wrapperStructOutput.cpp
    wrapperStructPose.cpp)

add_library(openpose_wrapper ${SOURCES})
target_link_libraries(openpose_wrapper openpose_core openpose_face openpose_filestream
    openpose_gui openpose_hand openpose_pose openpose_producer openpose_thread
    openpose_tracking openpose_utilities)

install(TARGETS openpose_wrapper
    EXPORT OpenPose
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib/openpose)
