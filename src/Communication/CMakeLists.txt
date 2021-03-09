set(COMMUNICATION_SRCS
    AsioService.cpp
    AsynchFileSender.cpp
    AsynchSender.cpp
    FileSender.cpp
    MulticastReceiverHandle.cpp
    PCapReader.cpp
)

add_library(communication STATIC
    ${COMMUNICATION_SRCS}
)

find_package(Boost 1.65.0)

target_include_directories(communication
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
    PRIVATE
        ${Boost_INCLUDE_DIRS}
)
