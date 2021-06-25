set(UNIT_TEST_LIST nfphmactest)

foreach (NAME IN LISTS UNIT_TEST_LIST)
    list(APPEND UNIT_TEST_SOURCE_LIST ${NAME}.test.cpp)
endforeach ()

set(TARGET_NAME tests)

message(STATUS "TARGET_NAME " ${PROJECT_NAME})
#target_link_directories(${PROJECT_NAME} PUBLIC ${PROJECT_NAME}/lib/)

add_executable(${TARGET_NAME}_bitmap
        ${UNIT_TEST_SOURCE_LIST} iso8583.test.cpp)

target_link_libraries(${TARGET_NAME}_bitmap PUBLIC Catch2WithMain cpp8583lib)

add_executable(${TARGET_NAME}_const const_generation.test.cpp)
target_link_libraries(${TARGET_NAME}_const PUBLIC Catch2WithMain)

add_executable(${TARGET_NAME}_mti mti.test.cpp)
target_link_libraries(${TARGET_NAME}_mti PUBLIC Catch2WithMain cpp8583lib)

# TODO: ?????
add_test(
        NAME ${TARGET_NAME}
        COMMAND ${TARGET_NAME} -o report.xml -r junit)
