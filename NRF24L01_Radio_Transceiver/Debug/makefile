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
NRF24L01_Radio_Transceiver.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
NRF24L01_Radio_Transceiver.list \

OBJCOPY_BIN += \
NRF24L01_Radio_Transceiver.bin \


# All Target
all: NRF24L01_Radio_Transceiver.elf secondary-outputs

# Tool invocations
NRF24L01_Radio_Transceiver.elf: $(OBJS) $(USER_OBJS) /home/jerryl/Git/Github_Public/BluePill-Examples/NRF24L01_Radio_Transceiver/STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "NRF24L01_Radio_Transceiver.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"/home/jerryl/Git/Github_Public/BluePill-Examples/NRF24L01_Radio_Transceiver/STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="NRF24L01_Radio_Transceiver.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

NRF24L01_Radio_Transceiver.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "NRF24L01_Radio_Transceiver.list"
	@echo 'Finished building: $@'
	@echo ' '

NRF24L01_Radio_Transceiver.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "NRF24L01_Radio_Transceiver.bin"
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
