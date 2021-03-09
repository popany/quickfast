set(COMMON_SRCS
    BitMap.cpp
    Decimal.cpp
    Profiler.cpp
    QuickFASTPch.cpp
    Types.cpp
    WorkingBuffer.cpp
    dllmain.cpp
)

add_library(common STATIC
    ${COMMON_SRCS}
)

target_include_directories(common
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
    PRIVATE
        ${Boost_INCLUDE_DIRS}
)

find_package(Boost 1.65.0 REQUIRED date_time)
