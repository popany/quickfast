set(EXAMPLES_SRCS
    ConsoleLock.cpp
    ExamplesPch.cpp
    MessageInterpreter.cpp
    MessagePerformance.cpp
    ValueToFix.cpp
)

add_library(examples STATIC
    ${EXAMPLES_SRCS}
)

target_include_directories(examples
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
)

target_link_libraries(examples
    PRIVATE
        codecs
)