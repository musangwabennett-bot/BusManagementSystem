# Bus Management System — OOP Java Assignment

## Project Structure
```
BusManagementSystem/
├── Dockerfile
├── pom.xml
└── src/main/java/com/busms/
    ├── interfaces/
    │   ├── Bookable.java
    │   └── Trackable.java
    ├── model/
    │   ├── Vehicle.java          ← Abstract class
    │   ├── BusManager.java       ← Extends Vehicle, implements Bookable & Trackable
    │   ├── CityBus.java
    │   ├── ExpressBus.java
    │   ├── LuxuryBus.java
    │   ├── SchoolBus.java
    │   ├── TouristBus.java
    │   ├── ElectricBus.java
    │   ├── Passenger.java
    │   ├── Driver.java
    │   ├── Route.java
    │   ├── Ticket.java
    │   ├── Booking.java
    │   ├── Payment.java
    │   ├── Schedule.java
    │   └── Maintenance.java
    ├── factory/
    │   └── BusFactory.java
    ├── report/
    │   └── ReportGenerator.java
    ├── util/
    │   └── InputValidator.java
    └── main/
        └── BusSystem.java        ← Main entry point

