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
Timer\ Input\ Capture.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Timer\ Input\ Capture.list \

OBJCOPY_BIN += \
Timer\ Input\ Capture.bin \


# All Target
all: Timer\ Input\ Capture.elf secondary-outputs

# Tool invocations
Timer\ Input\ Capture.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/Timer\ Input\ Capture/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Timer Input Capture.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/Timer Input Capture/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Timer Input Capture.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Timer\ Input\ Capture.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Timer Input Capture.list"
	@echo 'Finished building: $@'
	@echo ' '

Timer\ Input\ Capture.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Timer Input Capture.bin"
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
