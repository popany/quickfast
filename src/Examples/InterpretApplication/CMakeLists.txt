set(INTERPRETAPPLICATION_SRCS
    InterpretApplication.cpp
    main.cpp
)

add_executable(interpretapplication 
    ${INTERPRETAPPLICATION_SRCS}
)

target_include_directories(interpretapplication
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
)

find_package(Boost 1.65.0 REQUIRED thread)

target_link_libraries(interpretapplication
    PRIVATE
        examples
        application
        Boost::thread
)
