project(GD32F3x0_standard_peripheral LANGUAGES C CXX ASM)

# Comment-out unused source files.
add_library(GD32F3x0_standard_peripheral OBJECT
	${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_adc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_cec.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_cmp.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_crc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_ctc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_dac.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_dbg.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_dma.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_exti.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_fmc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_fwdgt.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_gpio.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_i2c.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_misc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_pmu.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_rcu.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_rtc.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_spi.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_syscfg.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_timer.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_tsi.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_usart.c
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Source/gd32f3x0_wwdgt.c
    )

target_include_directories(GD32F3x0_standard_peripheral PUBLIC
    ${DRIVERS_DIR}/GD32F3x0_standard_peripheral/Include
    )

# CMSIS header only library is linked.
target_link_libraries(GD32F3x0_standard_peripheral PUBLIC CMSIS)
