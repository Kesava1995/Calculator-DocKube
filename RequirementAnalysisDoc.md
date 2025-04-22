Requirement Analysis Document


1. Project Title
Advanced Web-Based Calculator with GCD/LCM Support

2. Introduction
The project enhances the standard calculator by introducing additional mathematical utilities — GCD and LCM calculations for integers and fractions. It provides a deeper demonstration of number theory application alongside standard arithmetic.

3. Objective
To develop a feature-rich calculator that supports:

Basic arithmetic operations

GCD and LCM calculations for integers

GCD and LCM for fractions (via normalization)

Clean, responsive UI accessible via browsers

4. Scope of the Project
Supports:

Basic arithmetic: +, −, ×, ÷

GCD/LCM of two integers

GCD/LCM of two fractions (by simplifying numerator/denominator separately)

Pure front-end (HTML/CSS/JS); no backend

User-triggered operations with results shown on-screen

5. Functional Requirements

ID			Requirement Description
FR01	Accepts user input via clickable buttons
FR02	Displays inputs and computed results
FR03	Performs +, −, ×, ÷ operations
FR04	Clears inputs when "C" is pressed
FR05	Calculates GCD for two integers
FR06	Calculates LCM for two integers
FR07	Calculates GCD of two fractions
FR08	Calculates LCM of two fractions
FR09	Displays errors (e.g., divide by 0, invalid format) gracefully




6. Non-Functional Requirements

ID		Description
NFR01	Loads and operates in under 2 seconds
NFR02	Responsive layout
NFR03	Structured and readable code
NFR04	Browser-compatible
NFR05	Handles input validation and user errors gracefully
7. Technologies to be Used

Component	Technology
UI			HTML, CSS
Logic		JavaScript
Hosting		GitHub Pages