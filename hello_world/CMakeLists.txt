set(SAMPLE sample.so_5.hello_world_s)
add_executable(${SAMPLE} main.cpp)
target_link_libraries(${SAMPLE} sobjectizer::StaticLib)
install(TARGETS ${SAMPLE} DESTINATION bin)

set(SAMPLE sample.so_5.hello_world)
add_executable(${SAMPLE} main.cpp)
target_link_libraries(${SAMPLE} sobjectizer::SharedLib)
install(TARGETS ${SAMPLE} DESTINATION bin)

