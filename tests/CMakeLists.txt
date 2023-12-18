set(TEST_FILES
    RiceCookerTest.cpp
)

add_executable(RiceCookerTest ${TEST_FILES})

target_link_libraries(RiceCookerTest GTest::GTest GTest::Main pthread)
