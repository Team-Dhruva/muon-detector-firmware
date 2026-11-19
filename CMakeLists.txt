cmake_minimum_required(VERSION 3.13)

include(pico_sdk_import.cmake)

project(muon_detector_firmware C CXX ASM)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

pico_sdk_init()

add_executable(muon_detector_firmware
    src/main.c
)

target_include_directories(muon_detector_firmware PRIVATE
    ${CMAKE_CURRENT_LIST_DIR}/include
)

target_link_libraries(muon_detector_firmware
    pico_stdlib
)

pico_add_extra_outputs(muon_detector_firmware)
