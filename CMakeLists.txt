CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

project(lab2 VERSION 0.1.0 LANGUAGES C CXX)

ADD_SUBDIRECTORY(googletest)

ADD_EXECUTABLE(c-echo
    main2.cpp
)

ADD_EXECUTABLE(c-echo-count
    main.cpp
)

ADD_EXECUTABLE(test
    test.cpp
)

TARGET_LINK_LIBRARIES(test gtest)
TARGET_COMPILE_DEFINITIONS(test PRIVATE gtest_disable_pthreads=ON)