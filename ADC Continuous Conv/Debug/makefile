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
ADC\ Continuous\ Conv.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
ADC\ Continuous\ Conv.list \

OBJCOPY_BIN += \
ADC\ Continuous\ Conv.bin \


# All Target
all: ADC\ Continuous\ Conv.elf secondary-outputs

# Tool invocations
ADC\ Continuous\ Conv.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/ADC\ Continuous\ Conv/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "ADC Continuous Conv.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/ADC Continuous Conv/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="ADC Continuous Conv.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

ADC\ Continuous\ Conv.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "ADC Continuous Conv.list"
	@echo 'Finished building: $@'
	@echo ' '

ADC\ Continuous\ Conv.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "ADC Continuous Conv.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
