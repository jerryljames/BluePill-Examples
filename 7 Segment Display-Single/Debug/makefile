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
7\ Segment\ Display-Single.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
7\ Segment\ Display-Single.list \

OBJCOPY_BIN += \
7\ Segment\ Display-Single.bin \


# All Target
all: 7\ Segment\ Display-Single.elf secondary-outputs

# Tool invocations
7\ Segment\ Display-Single.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/7\ Segment\ Display-Single/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "7 Segment Display-Single.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/7 Segment Display-Single/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="7 Segment Display-Single.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

7\ Segment\ Display-Single.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "7 Segment Display-Single.list"
	@echo 'Finished building: $@'
	@echo ' '

7\ Segment\ Display-Single.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "7 Segment Display-Single.bin"
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
