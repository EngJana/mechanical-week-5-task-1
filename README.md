# mechanical-week-5-task-1

smart methods internship week 5 - mechanical task 1: 4 gears with 18:1 ratio 

# Blender Mechanical Gears Animation

This project demonstrates how to create and animate mechanical gears in Blender with a specific gear ratio. The gears are set up to achieve a total ratio of 1:18 using four gears.

## Gear Specifications

1. **Gear A**: 10 teeth
2. **Gear B**: 60 teeth (ratio 6:1 with Gear A)
3. **Gear C**: 40 teeth (ratio 2:3 with Gear B)
4. **Gear D**: 180 teeth (ratio 9:2 with Gear C)

### Overall Ratio Calculation

\[ \text{Total Ratio} = \frac{60}{10} \times \frac{40}{60} \times \frac{180}{40} = 6 \times \frac{2}{3} \times \frac{9}{2} = 18 \]

## Setup Instructions

### 1. Add Gears

1. Open Blender.
2. Go to `Edit` > `Preferences` > `Add-ons`.
3. Enable `Add Mesh: Extra Objects`.
4. In the 3D Viewport, go to `Add` > `Mesh` > `Gears` to add the gears.
5. Set the number of teeth for each gear as specified:
   - Gear A: 10 teeth
   - Gear B: 30 teeth
   - Gear C: 15 teeth
   - Gear D: 45 teeth

### 2. Position Gears

1. Use the `Move` and `Rotate` tools to position the gears so their teeth interlock correctly.
2. Ensure the gears are aligned and meshed properly for smooth animation.
   
#### Step-by-Step Animation

1. **Add Drivers for Other Gears**:
   - Select Gear D.
   - Go to the `Object Properties` panel.
   - Right-click on the Z rotation axis and choose `Add Driver`.
   - In the driver editor, set the driver type to `Scripted Expression`.
   - Set the variable `var` to the previous gear in the sequence.
   - Use the following expressions for the gears:
     - Gear D: `var / (9/2)` (ratio with Gear C)
     - Gear C: `var / (2/3)` (ratio with Gear B)
     - Gear B: `var / (6/1)` (ratio with Gear A)
    
2. **Set Keyframes for Intermediate Positions**:
   - The timeline frame is set to 0
   - Press `A` to select all gears.
   - Press `I` to insert keyframes at the starting position.
   - Move the timeline to frame 60.
   - Rotate Gear A.
   - Press `A` then `I` to insert keyframes at the new position.
   - Continue this process until you achieve a full rotation in Gear D.
