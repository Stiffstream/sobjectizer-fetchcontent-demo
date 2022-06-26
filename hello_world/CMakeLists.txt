set(SAMPLE sample.so_5.hello_world)
add_executable(${SAMPLE} main.cpp)
target_link_libraries(${SAMPLE} sobjectizer::StaticLib)
install(TARGETS ${SAMPLE} DESTINATION bin)

