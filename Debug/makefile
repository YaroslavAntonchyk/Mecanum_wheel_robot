################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F3xx_HAL_Driver/Src/subdir.mk
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
Mecanum_wheel_robot.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Mecanum_wheel_robot.list \

OBJCOPY_BIN += \
Mecanum_wheel_robot.bin \


# All Target
all: Mecanum_wheel_robot.elf secondary-outputs

# Tool invocations
Mecanum_wheel_robot.elf: $(OBJS) $(USER_OBJS) F:\STM_projects\Cube\Mecanum_wheel_robot\STM32F303RETX_FLASH.ld
	arm-none-eabi-gcc -o "Mecanum_wheel_robot.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"F:\STM_projects\Cube\Mecanum_wheel_robot\STM32F303RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Mecanum_wheel_robot.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Mecanum_wheel_robot.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Mecanum_wheel_robot.list"
	@echo 'Finished building: $@'
	@echo ' '

Mecanum_wheel_robot.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Mecanum_wheel_robot.bin"
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
