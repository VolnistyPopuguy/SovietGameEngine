add_executable(Engine_test EngineTest.cpp)
target_link_libraries(Engine_test Boost::Boost Engine)
message(STATUS ${CMAKE_CXX_STANDARD})

add_test(NAME Engine_test COMMAND $<TARGET_FILE:Engine_test>)

file(COPY test_file.txt DESTINATION ${CMAKE_CURRENT_BINARY_DIR})

add_subdirectory(test_dir)
add_subdirectory(ImportTest)
