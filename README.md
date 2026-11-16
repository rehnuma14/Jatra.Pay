# Jatra.Pay 🚌💳

**Jatra.Pay** is a cashless public transport fare payment prototype designed to modernize local commuting in Bangladesh (featuring local Chattogram routes such as GEC, Bahaddarhat, Muradpur, Oxygen, Chawkbazar, and Station Road). 

Built as an Object-Oriented Programming (OOP) project and visual prototype, Jatra.Pay simulates a unified digital fare payment workflow supporting both **QR Code** payments (for smartphone users) and **USSD** payments (for feature phone users without internet access).

---

## 🌟 Key Features

* **Dual Payment Modes:** Supports simulated **QR** and **USSD** payment workflows to ensure accessibility for all commuters.
* **Route & Fare Selection:** Pre-configured with local city stops (`GEC`, `Bahaddarhat`, `Muradpur`, `Oxygen`, `Chawkbazar`, `Station Road`) with custom input support.
* **Input Validation:** Ensures starting and destination stops are non-empty, distinct, and that the fare falls within a valid range (`1 - 100 BDT`).
* **Instant Digital Receipts:** Generates timestamped payment confirmation dialogs/modals upon successful transaction simulation.
* **Live Transaction History:** Maintains an in-session log of completed rides and fare payments.
* **Dual Implementations:** Includes both a **Java Swing** desktop application and a **Browser-based (HTML/CSS/JS)** web mockup.

---

## 🏗️ Architecture & OOP Design

The core Java implementation (`JatraPay.java`) demonstrates fundamental Object-Oriented Programming principles—**Encapsulation**, **Inheritance**, and **Polymorphism**—through a clean, modular class structure:

* **`TransportService`**: Base class encapsulating route details and base fare calculation.
* **`PremiumService`**: Extends `TransportService` to override fare calculation with additional premium service charges.
* **`Passenger`**: Encapsulates commuter details (name and passenger category).
* **`Payment`**: Handles payment method selection (`QR` / `USSD`) and simulates payment authorization.
* **`TransactionController`**: Coordinates the interaction between `Passenger`, `TransportService`, and `Payment` to process transactions and return status updates.
* **`JatraPay`**: The main Swing GUI class providing a split-panel interface (Transaction Form on the left, Transaction History log on the right).

---

## 📂 Project Structure

```text
Jatra.Pay/
├── JatraPay.java       # Primary Java Swing desktop application & OOP domain models
├── index.html          # Browser-based web prototype (HTML/CSS/JS)
└── README.md           # Project documentation
```

---

## 🚀 How to Run

### 1. Java Swing Desktop Application
**Prerequisites:** Java Development Kit (JDK 8 or higher) installed on your machine. No external libraries or build tools are required.

1. Open your terminal or command prompt and navigate to the project directory:
   ```bash
   cd path/to/Jatra.Pay
   ```
2. Compile the Java source file:
   ```bash
   javac JatraPay.java
   ```
3. Run the application:
   ```bash
   java JatraPay
   ```

### 2. Web Prototype (`index.html`)
1. Locate `index.html` in the repository root.
2. Double-click the file to open it directly in any modern web browser (Chrome, Firefox, Edge, Safari), or serve it using a local development server (e.g., VS Code Live Server).

---

## 📖 Usage Flow

1. **Select Locations:** Choose or type a **Starting Location** and a **Destination** (must be different).
2. **Enter Fare:** Input a valid fare amount between `1` and `100` TK.
3. **Choose Payment Method:** Select either **QR** or **USSD**.
4. **Process Payment:** Click **Process** to validate inputs, view your instant digital receipt, and record the trip in the **Transaction History** panel.

---

## ⚠️ Project Scope & Limitations

* **Prototype Status:** This repository is an educational/demonstration prototype built to showcase UI flow and OOP architecture.
* **No Persistence or Live Gateways:** Transactions are simulated in memory; there is no connected database (MySQL/PostgreSQL), REST API backend, or live mobile financial service (MFS) / telecom USSD gateway integration.

---

## 🔮 Future Roadmap

* [ ] **Backend & Database Integration:** Connect to a Spring Boot / Node.js REST API with PostgreSQL or MySQL for persistent user accounts and trip logs.
* [ ] **Passenger Discounts & Tiers:** Integrate automated student and senior citizen fare discounts into the UI flow.
* [ ] **Live QR & USSD Gateways:** Integrate dynamic QR code generation/scanning and telecom USSD APIs.
* [ ] **Operator Dashboard:** Expand the web portal into a full analytics dashboard for transport owners and city authorities.

---

## 📄 License

This project is open-source and available for educational and demonstration purposes.
