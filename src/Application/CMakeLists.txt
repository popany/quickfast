set(APPLICATION_SRCS
    CommandArgParser.cpp
    DNDecoderConnectionImpl.cpp
    DecoderConnection.cpp
)

add_library(application STATIC
    ${APPLICATION_SRCS}
)

target_link_libraries(codecs
    PRIVATE
        common
        Communication
)

find_package(Boost 1.65.0)

target_include_directories(application
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
    PRIVATE
        ${Boost_INCLUDE_DIRS}
)
