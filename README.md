# Online Booking Table System

This is an object-oriented restaurant reservation system that allows customers to search branches, view available tables, book reservations, and make online payments. Admin users can approve or reject bookings. The system demonstrates clean UML modeling with interface usage and multi-branch support.

---

## 📌 Features

### 👤 Customer Functions
- Register and login
- Search restaurant branches by city
- View available tables by time
- Make table reservations
- Make online payments
- Cancel reservations

### 🛠️ Admin Functions
- View and manage booking requests
- Approve or reject bookings
- Confirm payment status

---

## 🧩 UML Design

### Use Case Diagram
- Actors: `Customer`, `Admin`
- Key Use Cases:
  - Book Table → Verify Availability
  - Make Payment → Online Payment → Confirm Payment
  - Cancel Booking → Approval Workflow

### Class Diagram Highlights
- Abstract base class: `User`
- Subclasses: `Customer`, `Admin`
- `Table` belongs to a `Branch`
- `Booking` links a `Customer`, `Table`, and `Payment`
- `Branch` supports location-based search
- Interfaces: `IBookable`, `IPaymentProcessor` for extendable behavior

---

## 🧠 Concepts Demonstrated

- Object-oriented principles (inheritance, association, abstraction)
- Interface design for flexible extension
- Multi-branch restaurant modeling
- UML diagrams: Use Case + Class Diagram
- Alignment with agile methodology and cultural inclusiveness (LO3–LO5)
