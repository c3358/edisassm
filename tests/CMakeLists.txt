CMAKE_MINIMUM_REQUIRED(VERSION 3.1)
set(CMAKE_CXX_STANDARD 11)
SET(EXECUTABLE_OUTPUT_PATH ${CMAKE_CURRENT_BINARY_DIR})
INCLUDE_DIRECTORIES(../include)

SET(test_x86_SOURCES    test_x86.cpp    ../Instruction.cpp ../Formatter.cpp)
SET(test_x86_64_SOURCES test_x86_64.cpp ../Instruction.cpp ../Formatter.cpp)

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wmissing-field-initializers -Wno-long-long -ansi -pedantic -W -Wall")

ADD_EXECUTABLE(test_x86 ${test_x86_SOURCES})
ADD_EXECUTABLE(test_x86_64 ${test_x86_64_SOURCES})

SET(CMAKE_BUILD_TYPE Debug)
