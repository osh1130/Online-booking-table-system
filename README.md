# Online Booking Table System

This is an object-oriented restaurant reservation system that allows customers to search branches, view available tables, book reservations, and make online payments. Admin users can approve or reject bookings. The system demonstrates clean UML modeling with interface-based extensibility, service-layer orchestration, and multi-branch support.

---

## 📌 Features

### 👤 Customer Functions
- Register and login
- Search restaurant branches by city and date
- View available tables
- Make table reservations
- Submit payment via credit card or PayPal
- Cancel reservations

### 🛠️ Admin Functions
- View and manage booking requests
- Approve or reject bookings
- Confirm payment status

---

## 🧩 UML Design Overview

### Use Case Diagram
- Actors: `Customer`, `Admin`
- Key Use Cases:
  - Book Table → Verify Availability
  - Make Payment → Online Payment → Confirm Payment
  - Cancel Booking → Approval Workflow

### Class Diagram Highlights
- Abstract base class: `User`
- Subclasses: `Customer`, `Admin`
- `Table` belongs to a `Branch`; availability checked via `IBookable`
- `Booking` links a `Customer`, `Table`, and `Payment`
- `CardDetails` / `PayPalDetails` are used to submit payment inputs
- `Payment` stores result only (not sensitive input)
- `ReservationService` coordinates core system actions
- Interfaces: `IBookable`, `IPaymentProcessor` support multiple implementations (e.g., `CreditCardProcessor`, `PayPalProcessor`)

---

### 🧠 Design Rationale

This system adopts a dual-layered modeling approach:

> Entity methods (e.g., `Customer.makeReservation`) reflect user-driven actions aligned with the use case perspective, while the `ReservationService` represents the system-level orchestration of those behaviors. This helps bridge object behavior and service flow, while maintaining clean separation of concerns.

---

## 💡 Concepts Demonstrated

- Object-oriented principles (inheritance, composition, abstraction)
- Interface-based design for behavioral extension
- Separation between user input models and business entities
- Centralized service coordination via `ReservationService`
- Secure handling of payment input vs. result storage
- UML diagrams: Use Case + Class Diagram
- Alignment with software engineering LO3–LO5
