# Smart Device Management System

A Python-based **Object-Oriented Programming (OOP)** project developed as part of the **EL 162 / 234 Object-Oriented Programming** course at the University of Mines and Technology (UMaT).

This project simulates a **Smart Home Device Management System**, where different smart devices can be managed through a simple menu-driven interface. It demonstrates the core principles of Object-Oriented Programming in Python, including **classes, objects, inheritance, encapsulation, constructors, properties, methods, and polymorphism**.

---

## Project Objectives

The project aims to demonstrate an understanding of:

- Variables and data types
- Input and output
- Conditional statements
- Loops
- Functions
- Classes and objects
- Constructors (`__init__`)
- Methods
- Inheritance
- Encapsulation
- Getters and Setters (`@property`)
- Using `super()`

---

## Features

The system allows users to:

- Display information about smart devices
- Turn devices ON and OFF
- Read temperature from a temperature sensor
- Increase and decrease light brightness
- Start and stop security camera recording
- Navigate through a user-friendly menu-driven interface

---

## Class Structure

### 1. SmartDevice (Parent Class)

The parent class contains common attributes and methods shared by all smart devices.

**Attributes**
- `name`
- `__device_id` *(private)*
- `__power_status` *(private)*

**Methods**
- `turn_on()`
- `turn_off()`
- `display_info()`

---

### 2. SecurityCamera (Child Class)

Inherits from `SmartDevice`.

**Additional Attribute**
- `recording_status`

**Methods**
- `start_recording()`
- `stop_recording()`

---

### 3. SmartLight (Child Class)

Inherits from `SmartDevice`.

**Additional Attribute**
- `brightness`

**Methods**
- `increase_brightness()`
- `decrease_brightness()`

Brightness is validated to ensure it remains between **0 and 100**.

---

### 4. TemperatureSensor (Child Class)

Inherits from `SmartDevice`.

**Additional Attribute**
- `temperature`

**Method**
- `read_temperature()`

---

## Object-Oriented Programming Concepts Demonstrated

### Encapsulation
Sensitive attributes such as **Device ID**, **Power Status**, and **Brightness** are declared private and accessed through `@property` getters and setters.

### Inheritance
All smart devices inherit common characteristics from the `SmartDevice` parent class, reducing code duplication.

### Constructors
Each class uses a constructor (`__init__`) to initialize its attributes.

### Method Overriding
Each child class extends the `display_info()` method to include information specific to that device.

### super()
The `super()` function is used in every child class constructor to initialize inherited attributes from the parent class.

---

## Menu Options

The application provides the following menu:

1. Display Device Information
2. Turn Device On
3. Turn Device Off
4. Read Temperature
5. Adjust Brightness
6. Start Recording
7. Stop Recording
8. Exit

---

## Project Structure

```
smart-device-management-system/
│
├── smart_device.py
├── README.md
└── .gitignore
```

---

## Technologies Used

- Python 3.x
- Object-Oriented Programming (OOP)

---

## How to Run the Program

1. Clone the repository.

```bash
git clone https://github.com/your-username/smart-device-management-system.git
```

2. Navigate into the project directory.

```bash
cd smart-device-management-system
```

3. Run the Python program.

```bash
python smart_device.py
```

---

## Sample Output

```
========== SMART DEVICE MANAGEMENT ==========
1. Display Device Information
2. Turn Device On
3. Turn Device Off
4. Read Temperature
5. Adjust Brightness
6. Start Recording
7. Stop Recording
8. Exit

Enter your choice:
```

---

## Validation Implemented

- Device ID cannot be empty.
- Brightness must remain between **0 and 100**.
- Power status accepts only **ON** or **OFF**.

These validations improve the reliability and integrity of the system.

---

## Learning Outcomes

Through this project, the following programming concepts were applied:

- Class design
- Object creation
- Data hiding
- Code reusability
- Inheritance
- Encapsulation
- Properties (`@property`)
- Menu-driven programming
- User interaction
- Modular programming

---

## Author

**David Aita**

Level 100 Electrical Engineering Student

University of Mines and Technology (UMaT)

Course: **EL 162 / 234 Object-Oriented Programming**

Lecturer: **Dr. Matthew Cobbinah**

---

## License

This project was developed strictly for academic purposes as part of the EL 162 / 234 Object-Oriented Programming Mini Project at UMaT.