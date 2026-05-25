file(GLOB TEST_SOURCES *.cpp)

add_executable(check ${TEST_SOURCES})

target_include_directories(check PUBLIC
    ${PROJECT_SOURCE_DIR}/banking
)

target_link_libraries(check
    banking
    gtest_main
    gmock
)

add_test(NAME check COMMAND check)
