set(TEST_FILES
    RiceCookerTest.cpp
)

add_executable(RiceCookerTest ${TEST_FILES})

target_include_directories(RiceCookerTest PRIVATE ${CMAKE_SOURCE_DIR}/src)

target_link_libraries(RiceCookerTest GTest::GTest GTest::Main pthread)
