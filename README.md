# Embedded_Unit_Testing
Creating a Unit Testing for A BareMetal function written in C , Using (AAA) Technique 
# Explaining
DC Voltage:
## Over Voltage Error Handling:
VMD_DcVoltage >= VMD_DCVM_CFG_MAX_VOLTAGE_THRESHOLD_SCALED_VOLTS
VMD_DcVoltage < VMD_DCVM_CFG_MAX_VOLTAGE_THRESHOLD_SCALED_VOLTS && VMD_DcVoltage > VMD_DCVM_CFG_MAX_CLEAR_VOLTAGE_THRESHOLD_SCALED_VOLTS
VMD_DcVoltage <= VMD_DCVM_CFG_MAX_CLEAR_VOLTAGE_THRESHOLD_SCALED_VOLTS
Under Voltage Error Handling:
VMD_DcVoltage <= VMD_DCVM_CFG_MIN_VOLTAGE_THRESHOLD_SCALED_VOLTS
VMD_DcVoltage > VMD_DCVM_CFG_MIN_VOLTAGE_THRESHOLD_SCALED_VOLTS && VMD_DcVoltage < VMD_DCVM_CFG_MIN_CLEAR_VOLTAGE_THRESHOLD_SCALED_VOLTS
VMD_DcVoltage >= VMD_DCVM_CFG_MIN_CLEAR_VOLTAGE_THRESHOLD_SCALED_VOLTS


## Battery Voltage:
Over Voltage:
battery_voltage_mV >= VMD_BVMD_CFG_VOLTAGE_MAXIMUM_THRESHOLD_MV
battery_voltage_mV <= VMD_BVMD_CFG_VOLTAGE_MAXIMUM_CLEAR_THRESHOLD_MV
Critical Over Voltage:
battery_voltage_mV >= VMD_BVMD_CFG_VOLTAGE_MAXIMUM_CRITICAL_THRESHOLD_MV
battery_voltage_mV <= VMD_BVMD_CFG_VOLTAGE_MAXIMUM_CRITICAL_CLEAR_THRESHOLD_MV
Under Voltage:
battery_voltage_mV <= VMD_BVMD_CFG_VOLTAGE_MINIMUM_THRESHOLD_MV
battery_voltage_mV >= VMD_BVMD_CFG_VOLTAGE_MINIMUM_CLEAR_THRESHOLD_MV
Critical Under Voltage:
battery_voltage_mV <= VMD_BVMD_CFG_VOLTAGE_MINIMUM_CRITICAL_THRESHOLD_MV
battery_voltage_mV >= VMD_BVMD_CFG_VOLTAGE_MINIMUM_CRITICAL_CLEAR_THRESHOLD_MV
Logic Supply Voltage (if VMD_LV_MODE is enabled):
Over Voltage:
BVMD_logic_supply_voltage_mV >= VMD_BVMD_CFG_RAW_LOGIC_SUPPLY_VOLTAGE_MAXIMUM_THRESHOLD
BVMD_logic_supply_voltage_mV < VMD_BVMD_CFG_LOGIC_SUPPLY_VOLTAGE_MAXIMUM_CLEAR_THRESHOLD
Under Voltage:
BVMD_logic_supply_voltage_mV <= VMD_BVMD_CFG_RAW_LOGIC_SUPPLY_VOLTAGE_MINIMUM_THRESHOLD
BVMD_logic_supply_voltage_mV >= VMD_BVMD_CFG_LOGIC_SUPPLY_VOLTAGE_MINIMUM_CLEAR_THRESHOLD




Event Types:
	
Event Type 1: DC over-voltage condition.
Event Type 2: DC under-voltage condition.
Event Type 3: Battery over-voltage condition.
Event Type 4: Battery critical over-voltage condition.
Event Type 5: Battery under-voltage condition.
Event Type 6: Battery critical under-voltage condition.
The status (1 or 0) indicates whether the condition is active (1) or cleared (0).

