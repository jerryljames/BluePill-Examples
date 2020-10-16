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
Blinky\ Label.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Blinky\ Label.list \

OBJCOPY_BIN += \
Blinky\ Label.bin \


# All Target
all: Blinky\ Label.elf secondary-outputs

# Tool invocations
Blinky\ Label.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/Blinky\ Label/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Blinky Label.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/Blinky Label/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Blinky Label.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Blinky\ Label.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Blinky Label.list"
	@echo 'Finished building: $@'
	@echo ' '

Blinky\ Label.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Blinky Label.bin"
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
