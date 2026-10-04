# Design log

## Why a tricopter
A tricopter needs one fewer lifting motor than a quadcopter. The trade-off is a tail that must tilt on a servo to steer yaw, which adds mechanical and control complexity. The design moved to three motors after one of the delivered motors turned out to be defective.

## Iterations
- **V1:** lightweight Y-frame concept. Established the open structure and the mass target.
- **V2:** tail servo platform. Removed the bulky motor compartment; the rear motor mounts to the servo horn.
- **V3:** 60 mm body with 8.6 mm motor bore. Cleaned the motor seat and strengthened the connected geometry.

## Control loop
Sensors, then state estimate, then control, then actuators, then feedback: the motion changes the next sensor reading.

## Yaw
The SG90 tilts the rear motor, sending part of its thrust sideways to create a yawing force.

## Mass
Parts 95 g (measured, without frame). Frame limit 15 g. Target total about 110 g. Thrust margin is still to be measured.
