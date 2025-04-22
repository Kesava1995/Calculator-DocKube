Technical Documentation
1. Overview
This document provides insights into the internal working of the calculator for developers, maintainers, or future extensions.

2. Technology Stack

Layer			Tech
UI				HTML5 + CSS3
Logic			JavaScript (Vanilla)
Hosting			GitHub Pages



3. Folder/File Structure
bash


/
├── index.html         # UI layout
├── style.css          # Styling and responsiveness
├── script.js          # Core logic (arithmetic + GCD/LCM)
└── README.md          # Project summary (optional)


5. Input Parsing Logic
Fraction inputs are split by /

Validated using regex or JavaScript split('/')

Inputs converted to integers before GCD/LCM processing



6. DOM Interaction
Event listeners attached to buttons

Inputs stored in variables

Final result shown by updating the innerText of the display element



7. Error Handling
Division by zero

Invalid fraction input (e.g., missing denominator)

Non-numeric values



8. Responsiveness
CSS media queries for layout adjustment

Flexbox/Grid used for button arrangement



9. Future Enhancements
History log of operations

Scientific functions (sin, cos, sqrt, etc.)

Expression parser to handle full arithmetic order

Keyboard input support