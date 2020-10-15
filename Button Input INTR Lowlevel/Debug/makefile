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
Button\ Input\ INTR\ Lowlevel.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Button\ Input\ INTR\ Lowlevel.list \

OBJCOPY_BIN += \
Button\ Input\ INTR\ Lowlevel.bin \


# All Target
all: Button\ Input\ INTR\ Lowlevel.elf secondary-outputs

# Tool invocations
Button\ Input\ INTR\ Lowlevel.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/Button\ Input\ INTR\ Lowlevel/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "Button Input INTR Lowlevel.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/Button Input INTR Lowlevel/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Button Input INTR Lowlevel.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Button\ Input\ INTR\ Lowlevel.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Button Input INTR Lowlevel.list"
	@echo 'Finished building: $@'
	@echo ' '

Button\ Input\ INTR\ Lowlevel.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Button Input INTR Lowlevel.bin"
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
