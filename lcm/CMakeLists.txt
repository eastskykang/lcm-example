set(TARGET_NAME example-msg)
include(${LCM_USE_FILE})

file(
        GLOB LCM_SOURCES #
        "${CMAKE_CURRENT_SOURCE_DIR}/*.lcm" #
)

lcm_wrap_types(
        CPP_HEADERS LCM_CPP_HEADERS
        ${LCM_SOURCES}
)

lcm_add_library(
        ${TARGET_NAME}
        CPP ${LCM_CPP_HEADERS}
)

target_include_directories(
        ${TARGET_NAME}
        INTERFACE $<BUILD_INTERFACE:${CMAKE_CURRENT_BINARY_DIR}>
)
