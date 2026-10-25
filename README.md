**Academic Session:** 2026/2027  
**Student Name:** MUHAMMAD IYAS SADIQ BIN MOHD HANAFIAH
**Student ID:** CI240003  
**Repository:** `bic21203-lab4a-javascript`

---

##  Overview

This repository contains the complete implementation for **Lab 4a** under `BIC21203 Web Development`. The lab focuses on fundamental modern client-side JavaScript techniques, including element selection, event listener binding with `addEventListener()`, safe text manipulation using `textContent`, input validation logic, and dynamic DOM element creation via loops.

---

##  Repository Structure

```text
bic21203-lab4a-javascript/
│
├── q1/
│   ├── q1.html          # HTML structure for Question 1
│   └── script1.js       # JS logic for interactive text changer
│
├── q2/
│   ├── q2.html          # HTML structure for Question 2
│   └── script2.js       # JS logic for smart number validator
│
├── q3/
│   ├── q3.html          # HTML structure for Question 3
│   └── script3.js       # JS logic for dynamic list generation
│
└── README.md            # Repository documentation
```

---

##  How to Run the Code

Since this lab uses standard modern HTML5 and client-side JavaScript without external library dependencies, you can run any of the questions using the following methods:

### Method 1: Using Live Server (Recommended)
1. Open this repository in **Visual Studio Code**.
2. Install the **Live Server** extension (by Extension ID: `ritwickdey.LiveServer`).
3. Right-click on the desired HTML file (`q1/q1.html`, `q2/q2.html`, or `q3/q3.html`) and select **Open with Live Server**.

### Method 2: Direct Browser Execution
1. Download or clone this repository to your local machine:
   ```bash
   git clone https://github.com/eyashanafiah/bic21203-lab4a-javascript-
   ```
2. Navigate to the desired folder (`q1`, `q2`, or `q3`).
3. Double-click the corresponding `.html` file to open it directly in any modern web browser (e.g., Chrome, Edge, Firefox).

---

##  Question Details & Output Screenshots

### Question 1 — Interactive Text Changer
* **Description:** Selects a paragraph element and updates its text content from `"Welcome to my website!"` to `"Hello there!"` upon clicking the "Change Message" button using `addEventListener()`.
* **Files:** `q1/q1.html`, `q1/script1.js`

#### Output Screenshots:
| Initial Load | After Button Click |
| :---: | :---: |
| ![Q1 Initial State](https://via.placeholder.com/400x200?text=Q1+Initial+State) | ![Q1 Modified State](https://via.placeholder.com/400x200?text=Q1+Modified+State) |

---

### Question 2 — Smart Number Validator
* **Description:** Takes user input and performs validation checks against empty inputs, non-numeric strings (e.g., `abc`), numbers below 10, numbers above 10, and numbers equal to 10 (including decimal inputs like `10.5`). Displays output dynamic status messages using safe `textContent` injection.
* **Files:** `q2/q2.html`, `q2/script2.js`

#### Output Screenshots / Test Cases:
| Test Case | Expected Result | Screenshot |
| :--- | :--- | :---: |
| **Empty Input** | `"Please enter a valid number!"` | ![Q2 Empty](https://via.placeholder.com/300x150?text=Q2+Empty+Input) |
| **Non-numeric (`abc`)** | `"Please enter a valid number!"` | ![Q2 Non-numeric](https://via.placeholder.com/300x150?text=Q2+Invalid+abc) |
| **Number `< 10` (e.g., `5`)** | `"The number is lower than 10"` | ![Q2 Lower](https://via.placeholder.com/300x150?text=Q2+Lower+Than+10) |
| **Number `= 10` (e.g., `10`)** | `"The number is equal to 10"` | ![Q2 Equal](https://via.placeholder.com/300x150?text=Q2+Equal+To+10) |
| **Number `> 10` (e.g., `15`)** | `"The number is higher than 10"` | ![Q2 Higher](https://via.placeholder.com/300x150?text=Q2+Higher+Than+10) |

---

### Question 3 — Dynamic Number Generator
* **Description:** Uses a `for` loop iterating from 1 through 5 to dynamically build `<li>` elements using `document.createElement()` and appends them to an ordered list (`<ol>`). Existing elements are cleared prior to generation to prevent duplicate lists on repeated clicks.
* **Files:** `q3/q3.html`, `q3/script3.js`

#### Output Screenshots:
| Initial State | Generated List Output |
| :---: | :---: |
| ![Q3 Initial](https://via.placeholder.com/400x200?text=Q3+Initial+State) | ![Q3 Generated](https://via.placeholder.com/400x200?text=Q3+Generated+List) |

---

##  Security & Code Quality Notes
* **XSS Prevention:** All dynamic updates use `textContent` instead of `innerHTML` to prevent Cross-Site Scripting (XSS) vulnerabilities when dealing with user inputs.
* **Event Listener Best Practices:** Native `addEventListener()` is used throughout instead of inline HTML event handlers (`onclick`) to ensure clear separation of concern between HTML structure and JavaScript behavior.
* **Defer Placement:** Scripts are included with the `defer` attribute or executed after DOM elements are ready to prevent null reference errors.
