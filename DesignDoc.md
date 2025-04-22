Design Document


1. Overview
This document outlines the system architecture and user interface design for the Web-Based Calculator. It provides a blueprint of how the application looks and functions internally.

2. System Architecture


+----------------------------+
|      User Interface       | (Buttons, Inputs, Output area)
+----------------------------+
|     Input Handler Layer   | (Capture and parse user input)
+----------------------------+
| Arithmetic & GCD/LCM Logic| (Core calculations for basic and advanced functions)
+----------------------------+
|     Output Display Layer  | (DOM manipulation to show result)
+----------------------------+

Components:
UI Layer: HTML elements and CSS styles used to present the calculator layout.

Input Handler: Captures button click events and passes data to the logic layer.

Logic Layer: Handles the core computation.

Display Layer: Updates the screen with the result/output.

3. UI Layout Sketch (Text-based)



 ____________________
|  Display: 123 + 5  |
|--------------------|
|  7  |  8  |  9  | / |
|--------------------|
|  4  |  5  |  6  | * |
|--------------------|
|  1  |  2  |  3  | - |
|--------------------|
|  0  |  .  |  =  | + |
|--------------------|
|         C (Clear)  |


 ____________________________
|     Display: 1/2 , 3/4     |
|----------------------------|
|  7  |  8  |  9  |   /      |
|  4  |  5  |  6  |   *      |
|  1  |  2  |  3  |   -      |
|  0  |  .  |  =  |   +      |
|----------------------------|
| GCD | LCM |Frac GCD|Frac LCM|
|------------  C  ------------|


4. CSS Design Considerations
Responsive grid layout using Flexbox or Grid

Rounded buttons, hover effects, and basic transitions

Mobile-first approach to make it usable on smaller screens


5. Logic Breakdown
GCD (Integers): Euclidean algorithm

LCM (Integers): (a × b) / GCD(a, b)

GCD (Fractions):

Normalize both fractions

GCD of numerators and LCM of denominators

LCM (Fractions):

Normalize both fractions

LCM of numerators and GCD of denominators