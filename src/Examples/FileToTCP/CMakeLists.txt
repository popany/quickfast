set(FILE_TO_TCP_SRCS
    FileToTCP.cpp
    main.cpp
)

add_executable(file_to_tcp
    ${FILE_TO_TCP_SRCS}
)

target_include_directories(file_to_tcp
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
)

find_package(Boost 1.65.0 REQUIRED thread)

target_link_libraries(file_to_tcp
    PRIVATE
        examples
        application
        Boost::thread
)
