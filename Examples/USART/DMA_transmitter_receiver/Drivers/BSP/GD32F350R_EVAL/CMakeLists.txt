project(GD32F350R_EVAL LANGUAGES C CXX ASM)

add_library(GD32F350R_EVAL OBJECT
    ${DRIVERS_DIR}/BSP/GD32F350R_EVAL/gd32f350r_eval.c
    )

target_include_directories(GD32F350R_EVAL PUBLIC
    ${DRIVERS_DIR}/BSP/GD32F350R_EVAL
    )

target_link_libraries(GD32F350R_EVAL PUBLIC GD32F3x0_standard_peripheral)
