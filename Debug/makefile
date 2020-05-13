################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
stm32_tim1ms.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
stm32_tim1ms.list \

OBJCOPY_HEX += \
stm32_tim1ms.hex \

OBJCOPY_BIN += \
stm32_tim1ms.bin \


# All Target
all: stm32_tim1ms.elf secondary-outputs

# Tool invocations
stm32_tim1ms.elf: $(OBJS) $(USER_OBJS) C:\Users\sdrshnptl\STM32CubeIDE\workspace_1.1.0\stm32_tim1ms\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "stm32_tim1ms.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\sdrshnptl\STM32CubeIDE\workspace_1.1.0\stm32_tim1ms\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="stm32_tim1ms.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

stm32_tim1ms.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "stm32_tim1ms.list"
	@echo 'Finished building: $@'
	@echo ' '

stm32_tim1ms.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "stm32_tim1ms.hex"
	@echo 'Finished building: $@'
	@echo ' '

stm32_tim1ms.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "stm32_tim1ms.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
