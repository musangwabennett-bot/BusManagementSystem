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
```

## OOP Concepts Demonstrated
| Concept        | Where                                      |
|----------------|--------------------------------------------|
| Encapsulation  | All model classes (private fields + getters/setters) |
| Abstraction    | `Vehicle.java` (abstract class)            |
| Interfaces     | `Bookable.java`, `Trackable.java`          |
| Inheritance    | BusManager → 6 subclasses                 |
| Polymorphism   | `BusFactory`, overridden methods           |
| Constructors   | Default + parameterized in every class     |
| Method Override| `toString()`, `calculateFare()`, `startVehicle()`, etc. |

---

## How to Build & Run

### Option A — Using Maven directly
```bash
# 1. Make sure Java 11+ and Maven 3.x are installed
java -version
mvn -version

# 2. Build the JAR
cd BusManagementSystem
mvn clean package -DskipTests

# 3. Run
java -jar target/bus-management-system.jar
```

### Option B — Using Docker (recommended for submission)
```bash
# 1. Build the Docker image
docker build -t bus-management-system .

# 2. Run interactively (required because of Scanner input)
docker run -it bus-management-system
```

---

## Submission Steps
1. Push this project to a **public GitHub repository**
2. Invite **kiyengobis@gmail.com** as a collaborator
3. Fill in the class Google Form with: **ID | Name | GitHub Repo Link**
4. Deadline: **Wednesday**

---

## Sample Interaction
```
Enter Bus Type: CITY
Enter Bus ID: BUS-001
Enter Bus Name: Kigali City Express
Enter Capacity: 45
Enter Driver Name: Jean Claude
Enter Bus Number: RAB-001A
Enter Route ID: R001

[RAB-001A] Starting city route on: City Loop
✔ Bus added successfully!
=== Vehicle Report ===
Bus Number  : RAB-001A
Driver      : Jean Claude
Route       : R001
Capacity    : 45
Booked Seats: 0
Status      : Running
Location    : Depot
Type        : City Bus
City Route  : City Loop
AC          : No
Stops       : 15
```
