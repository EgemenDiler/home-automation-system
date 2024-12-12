# Home Automation System - State Table

| Current State       | Input (Motion)  | Input (Light)  | Input (Temp)   | Next State       | Output (Lights) | Output (Heater) |
|---------------------|-----------------|----------------|----------------|------------------|-----------------|-----------------|
| Idle                | No              | Low            | Low            | Idle             | OFF             | OFF             |
| Idle                | Yes             | Low            | Low            | Motion Detected  | ON              | OFF             |
| Motion Detected     | Yes             | Low            | High           | Heating On       | ON              | ON              |
| Motion Detected     | No              | Low            | Low            | Light Control    | OFF             | OFF             |
| Light Control       | No              | Low            | Low            | Idle             | OFF             | OFF             |
| Heating On          | No              | Low            | High           | Idle             | OFF             | ON              |
