# Online Booking Table System

This is an object-oriented project for a restaurant **Online Booking Table System**. It allows customers to reserve tables at a restaurant, make payments online, and manage bookings. Admin users can review and approve or reject bookings. The system also integrates use case and class modeling in UML.

---

## 📌 Project Features

### 👤 For Customers
- Register and Login
- Search restaurant branches
- View table availability
- Book a table / make a reservation
- Make online payment
- Cancel booking

### 🛠️ For Admins
- View booking requests
- Approve or reject bookings
- Confirm payment status

---

## 🧩 UML Diagrams

### ✅ Use Case Diagram
- Actors: `Customer`, `Admin`
- Core Use Cases:
  - Book Table / Make Reservation
  - Make Payment → Online Payment → Confirm Payment
  - Cancel Booking → Approval Workflow
  - Includes: `Verify Table Availability`, `Approve/Reject Booking`

### ✅ Class Diagram
Includes:
- `User` (abstract base class)
- `Customer` / `Admin` (inherit from User)
- `Table`
- `Booking`
- `Payment`

Key relationships:
- One Customer can have many Bookings and Payments
- Booking is linked to one Table and one Payment

---

## 🧠 Key Concepts Demonstrated

- Object-oriented design (inheritance, relationships)
- UML modeling: Use Case + Class Diagram
- Software engineering principles (LO3, LO4, LO5)
- Agile sprint alignment & documentation
- Culturally informed teamwork and system considerations
