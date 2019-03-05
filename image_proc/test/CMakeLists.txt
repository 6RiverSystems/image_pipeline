find_package(rostest REQUIRED)
find_package(catkin REQUIRED roscpp image_transport cv_bridge camera_calibration_parsers)

include_directories(include ${catkin_INCLUDE_DIRS})

#catkin_add_gtest(image_proc_rostest rostest.cpp)
#target_link_libraries(image_proc_rostest ${catkin_LIBRARIES}  ${Boost_LIBRARIES})
add_rostest_gtest(image_proc_test_rectify test_rectify.xml test_rectify.cpp)
target_link_libraries(image_proc_test_rectify ${catkin_LIBRARIES})
