################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include src/subdir.mk
-include emlib/subdir.mk
-include FreeRTOS/efm32gg/subdir.mk
-include Drivers/subdir.mk
-include CMSIS/EFM32GG/subdir.mk
-include BSP/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 

# All Target
all: STK3700_freertos_blink_2.axf

# Tool invocations
STK3700_freertos_blink_2.axf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM C Linker'
	arm-none-eabi-gcc -g3 -gdwarf-2 -mcpu=cortex-m3 -mthumb -T "STK3700_freertos_blink_2.ld" -Xlinker --gc-sections -Xlinker -Map="STK3700_freertos_blink_2.map" --specs=nano.specs -o STK3700_freertos_blink_2.axf "./BSP/bsp_stk_leds.o" "./BSP/bsp_trace.o" "./CMSIS/EFM32GG/startup_gcc_efm32gg.o" "./CMSIS/EFM32GG/system_efm32gg.o" "./Drivers/sleep.o" "./FreeRTOS/efm32gg/croutine.o" "./FreeRTOS/efm32gg/event_groups.o" "./FreeRTOS/efm32gg/heap_1.o" "./FreeRTOS/efm32gg/list.o" "./FreeRTOS/efm32gg/port_gcc.o" "./FreeRTOS/efm32gg/queue.o" "./FreeRTOS/efm32gg/tasks.o" "./FreeRTOS/efm32gg/timers.o" "./emlib/em_adc.o" "./emlib/em_assert.o" "./emlib/em_burtc.o" "./emlib/em_cmu.o" "./emlib/em_core.o" "./emlib/em_dac.o" "./emlib/em_emu.o" "./emlib/em_gpio.o" "./emlib/em_i2c.o" "./emlib/em_leuart.o" "./emlib/em_rmu.o" "./emlib/em_rtc.o" "./emlib/em_system.o" "./emlib/em_usart.o" "./emlib/em_wdog.o" "./src/low_power_tick_management.o" "./src/main.o" -Wl,--start-group -lgcc -lc -lnosys -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

	@echo 'Building hex file: STK3700_freertos_blink_2.hex'
	arm-none-eabi-objcopy -O ihex "STK3700_freertos_blink_2.axf" "STK3700_freertos_blink_2.hex"
	@echo ' '

	@echo 'Building bin file: STK3700_freertos_blink_2.bin'
	arm-none-eabi-objcopy -O binary "STK3700_freertos_blink_2.axf" "STK3700_freertos_blink_2.bin"
	@echo ' '

	@echo 'Building s37 file: STK3700_freertos_blink_2.s37'
	arm-none-eabi-objcopy -O srec "STK3700_freertos_blink_2.axf" "STK3700_freertos_blink_2.s37"
	@echo ' '

	@echo 'Running size tool'
	arm-none-eabi-size "STK3700_freertos_blink_2.axf" -A
	@echo ' '

# Other Targets
clean:
	-$(RM) $(EXECUTABLES)$(OBJS)$(C_DEPS) STK3700_freertos_blink_2.axf
	-@echo ' '

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
