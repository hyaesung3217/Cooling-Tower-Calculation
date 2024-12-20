
# Cooling-Tower-Optimization

Once the model is created using the "CoolingTowerParametrization" file, this section performs energy optimization calculations based on the user-defined inputs and the generated model.

### Model and Data Files
The model should be created and loaded (polynomial_regression_model.pkl) along with the polynomial transformer file (polynomial_features.pkl). These files must be placed directly under the `sample_data` folder, which can be accessed via the file icon located on the left.

### Polynomial Equation
With the model generated from the file "CoolingTowerParametrization," it is possible to extract and export a matrix of coefficients and related variables. A message will be printed: "Equation exported as 'polynomial_equation.xlsx'," and it will be located in the left column.

### User-Defined Inputs and Constants
The following inputs, constants, and functions are used across different programs. Users can modify their content, but changes should be made carefully as they affect other parts of the code. Inputs can be entered manually or via sliders:

- **Inputs**: 
  - Water flow
  - Wet bulb temperature
  - Number of streams
  - Minimum fan speed percentage
  - Initial range value (iteration)

- **User-Defined Constants** (values can be changed):
  - CHILLER_CAPACITY_UNIT_TR
  - SPECIFIC_HEAT
  - CHILLER_WATER_FLOW
  - FAN_POWER
  - WATER_DENSITY
  - GRAVITY
  - PUMP_HEAD
  - PUMP_WATER_FLOW
  - PUMP_EFFECTIVENESS

### User-Defined Functions
These functions are used for various calculations:
- `chiller_consumption_calculation` – To calculate chiller consumption
- `new_range_calculation` – To calculate a new range value after one iteration
- `pump_calculation` – To calculate pump consumption
- `effectiveness_calculation` – To calculate efficiency
- `total_consumption_calculation` – To calculate total consumption
- `fan_consumption_calculation` – To calculate fan consumption
- `heat_rejected_by_condenser_calculation` – To calculate heat rejected by the chiller condenser
- `new_range_calculation` – Encapsulates all the above functions to output effectiveness, new range, total consumption, fan consumption, chiller consumption, and pump consumption.

**Note**: Ensure constants and functions are defined before using any section. If a function error occurs (e.g., function not found), execute the definition section again.

### Visualization Plots
1. **Fan Speed vs Total Consumption**: 
   - Generate a plot displaying the consumption graphs at various fan speeds (chiller, pump, fan, total consumption). The goal is to identify the optimal point of minimum consumption.

2. **Fan Speed vs Total Consumption vs Flow Rate (3D)**: 
   - Generate a 3D plot indicating the optimal point (minimum consumption) based on various flow rate and fan speed values.

3. **Fan Speed vs Wet Bulb Temperature**: 
   - Generate a 2D plot showing the fan speed values at different wet bulb temperature values when consumption is minimized.

4. **Cold Water Temperature vs Wet Bulb Temperature**: 
   - Generate a 2D plot showing the cold water temperature values at different wet bulb temperature values when consumption is minimized.

5. **Minimum Total Consumption vs Wet Bulb Temperature**: 
   - Generate a 2D plot showing the minimum total consumption values at different wet bulb temperature levels when consumption is minimized.

