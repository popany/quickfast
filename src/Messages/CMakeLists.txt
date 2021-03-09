set(MESSAGES_SRCS
    Field.cpp
    FieldAscii.cpp
    FieldByteVector.cpp
    FieldDecimal.cpp
    FieldGroup.cpp
    FieldIdentity.cpp
    FieldInt16.cpp
    FieldInt32.cpp
    FieldInt64.cpp
    FieldInt8.cpp
    FieldSequence.cpp
    FieldSet.cpp
    FieldString.cpp
    FieldUInt16.cpp
    FieldUInt32.cpp
    FieldUInt64.cpp
    FieldUInt8.cpp
    FieldUtf8.cpp
    Message.cpp
    MessageAccessor.cpp
    MessageBuilder.cpp
    MessageFormatter.cpp
)

add_library(messages STATIC
    ${MESSAGES_SRCS}
)

target_include_directories(messages
    PUBLIC
        ${CMAKE_CURRENT_SOURCE_DIR}/../
)
