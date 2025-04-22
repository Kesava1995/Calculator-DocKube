Test Cases Document

1. Overview
Testing both basic operations and GCD/LCM calculations for integers and fractions.

2. Test Cases
A. Basic Arithmetic Tests

TC ID	Operation	Input	Expected Output
TC01	Addition	4 + 3	7
TC02	Subtraction	10 - 6	4
TC03	Multiplication	5 * 6	30
TC04	Division	12 / 3	4
TC05	Divide by zero	5 / 0	Error or Infinity


B. GCD/LCM (Integer)

TC ID	Operation			Input	Expected Output
TC06	GCD					24, 36	12
TC07	LCM					4, 6	12
TC08	GCD with 0			0, 10	10
TC09	LCM with 0			0, 15	0



C. GCD/LCM (Fractions)

TC ID	Operation				Input			Expected Output
TC10	GCD of Fractions		2/3, 4/9		GCD: 2/9
TC11	LCM of Fractions		2/5, 3/10		LCM: 1/10 
TC12	GCD improper fractions	7/4, 5/6		GCD: 1/12
TC13	LCM improper fractions	7/4, 5/6		LCM: 35/12


3. Testing Strategy
Manual Testing:

Input combinations verified via browser console and UI.

Cross-checked results with math tools like WolframAlpha.

Responsive Design:

Verified layout on Chrome dev tools (mobile + desktop)