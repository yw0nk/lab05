
file(GLOB TEST_SOURCES "*.cpp")

add_executable(runTests ${TEST_SOURCES})


target_link_libraries(runTests
    gtest_main
    print
)

include(GoogleTest)
gtest_discover_tests(runTests)
