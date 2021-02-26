################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
S4mini_Motor_030.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
S4mini_Motor_030.list \

OBJCOPY_BIN += \
S4mini_Motor_030.bin \


# All Target
all: S4mini_Motor_030.elf secondary-outputs

# Tool invocations
S4mini_Motor_030.elf: $(OBJS) $(USER_OBJS) D:\U\Appo_Motor_030\S4mini_Motor_030\STM32F030C8TX_FLASH.ld
	arm-none-eabi-gcc -o "S4mini_Motor_030.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0 -T"D:\U\Appo_Motor_030\S4mini_Motor_030\STM32F030C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="S4mini_Motor_030.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

S4mini_Motor_030.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "S4mini_Motor_030.list"
	@echo 'Finished building: $@'
	@echo ' '

S4mini_Motor_030.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "S4mini_Motor_030.bin"
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
