add_executable(listener listener.cpp)
target_link_libraries(listener PUBLIC lcm example-msg)

add_executable(read-log read_log.cpp)
target_link_libraries(read-log PUBLIC lcm example-msg)

add_executable(sender send_message.cpp)
target_link_libraries(sender PUBLIC lcm example-msg)
