# Test plan

1. **Pre-flight:** check the frame, propellers, power, radio link and sensor readings.
2. **Manual flight:** the ground station sends commands by radio. Manual input is the main way to test response and trim.
3. **Autonomous climb (planned):** a laptop-set altitude is the climb target, using BMP280 pressure data.
4. **Hold and return (planned):** a controlled hold and descent once the flight logic is validated.

## Test ladder
| Height | Purpose |
|---|---|
| 2 m | First low hover |
| 5 m | Response check |
| 10 m | Stability check |
| 15 m | Control validation |
| 20-30 m | Full mission, only after all earlier steps pass |

Radio range is a design goal until it is measured in the final environment. 
