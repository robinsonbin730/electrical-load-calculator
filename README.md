# ⚡ Electrical Load Calculator

A modern Python desktop application that calculates electrical loads for residential and commercial circuits. The application helps electricians, apprentices, and electrical students estimate current, select standard breaker sizes, recommend conductor sizes, and export calculation reports.

> **Disclaimer:** This application is intended for educational purposes and preliminary load calculations. Final electrical designs must comply with the latest National Electrical Code (NEC), local building codes, and be reviewed by a qualified electrician or engineer.

---

# Features

* Calculate electrical current from connected load
* Supports multiple voltages:

  * 120 V
  * 208 V
  * 240 V
  * 277 V
  * 480 V
* Automatically recommends the next standard breaker size
* Recommends conductor (wire) size
* Calculates kVA
* Calculates design current using the 125% continuous-load rule
* Export results to Microsoft Excel
* Modern graphical interface built with CustomTkinter
* Simple, fast, and easy to use

---

# Example Calculation

### Inputs

| Parameter      |  Value |
| -------------- | -----: |
| Voltage        |  120 V |
| Connected Load | 1800 W |

### Results

| Calculation           |  Result |
| --------------------- | ------: |
| Current               |  15.0 A |
| Design Current (125%) |  18.8 A |
| Recommended Breaker   |    20 A |
| Recommended Wire      |  12 AWG |
| Apparent Power        | 1.8 kVA |

---

# Project Structure

```text
electrical-load-calculator/
│
├── main.py
├── config.py
├── requirements.txt
├── README.md
├── LICENSE
│
├── calculators/
│      load_calculator.py
│      breaker.py
│      wire_size.py
│
├── gui/
│      app.py
│      styles.py
│
├── utils/
│      export_excel.py
│      validators.py
│
├── data/
│      breaker_sizes.csv
│      wire_sizes.csv
│
├── images/
│      screenshot.png
│
└── tests/
       test_load.py
```

---

# How It Works

The calculator performs the following steps:

1. User selects the operating voltage.
2. User enters the connected electrical load in watts.
3. Current is calculated using:

```
Current (A) = Watts ÷ Voltage
```

4. For continuous loads, the application calculates the design current:

```
Design Current = Current × 1.25
```

5. The application recommends the next standard circuit breaker.

6. Based on the breaker size, the recommended conductor size is displayed.

7. Results can be exported to an Excel spreadsheet.

---

# Technologies

* Python 3.12+
* CustomTkinter
* Pandas
* OpenPyXL
* NumPy
* Pillow

---

# Installation

Clone the repository:

```bash
git clone https://github.com/robinsonbin730/electrical-load-calculator.git
```

Open the project directory:

```bash
cd electrical-load-calculator
```

Install required packages:

```bash
pip install -r requirements.txt
```

Run the application:

```bash
python main.py
```

---

# Screenshots

## Main Window

*(Add a screenshot after running the application.)*

```
 ----------------------------------------------------
            Electrical Load Calculator
 ----------------------------------------------------

 Voltage
 [120 V ▼]

 Connected Load (Watts)

 [1800]

 -----------------------------------------

 Current

 15.0 A

 Design Current

 18.8 A

 Breaker

 20 A

 Wire

 12 AWG

 -----------------------------------------

        [ Calculate ]

        [ Export to Excel ]

        [ Reset ]

 ----------------------------------------------------
```

---

# Future Enhancements

* Voltage Drop Calculator
* Conduit Fill Calculator
* NEC ampacity tables
* Panel load calculations
* Demand factor calculations
* PDF report generation
* Dark mode
* Multi-language support
* Save calculation history
* Print reports

---

# License

This project is released under the MIT License.

---

# Author

**Tung Thanh Truong**

Electrical Trainee
Center for Employment Training (CET)

GitHub: https://github.com/robinsonbin730

---

# Acknowledgments

This project was created to strengthen programming skills while applying electrical engineering concepts learned through hands-on electrician training. It demonstrates the integration of software development with practical electrical calculations commonly used by electricians and apprentices.
