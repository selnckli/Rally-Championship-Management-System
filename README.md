# Rally Championship Management System

A Java application that manages a rally championship by registering drivers, recording race results, and calculating championship standings. Built to demonstrate SOLID principles, use of static members, and the Singleton pattern.

---

## Features

- **Driver Management**  
  - Register drivers with name, country, and total points.  
  - Add points to drivers after each race.

- **Car Class Hierarchy**  
  - `RallyCar` (abstract) with properties: make, model, horsepower.  
  - `GravelCar` and `AsphaltCar` extend `RallyCar`, each implementing a custom `calculatePerformance()` algorithm.

- **Championship Management (Singleton)**  
  - `ChampionshipManager` ensures a single instance holds all drivers and race results.  
  - Static methods to get standings, find the leader, and compute total points.

- **Race Results (Interface Segregation)**  
  - `RaceResult` interface defines methods for recording/retrieving race data.  
  - `RallyRaceResult` implements `RaceResult`.

- **Statistics Utility (Static Utility Class)**  
  - `ChampionshipStatistics` offers static methods to calculate average points per driver, determine the most successful country, and count total races.

- **Simulation (Main Class)**  
  - Configures the championship, creates drivers and cars, simulates races on different surfaces, and outputs detailed results and statistics.

## Expected Output

```text
1. Sébastien Ogier (France): 40 points
2. Kalle Rovanperä (Finland): 40 points
3. Ott Tänak (Estonia): 30 points
4. Thierry Neuville (Belgium): 30 points

===== CHAMPIONSHIP LEADER =====
Sébastien Ogier with 40 points

===== CHAMPIONSHIP STATISTICS =====
Total Drivers: 4
Total Races: 2
Average Points Per Driver: 35.00
Most Successful Country: Finland
Total Championship Points: 140

===== RACE RESULTS =====
Race: Rally Finland (Jyväskylä)
  Position 1: Sébastien Ogier – 25 points
  Position 2: Ott Tänak – 18 points
  Position 3: Kalle Rovanperä – 15 points
  Position 4: Thierry Neuville – 12 points

Race: Monte Carlo Rally (Monaco)
  Position 1: Kalle Rovanperä – 25 points
  Position 2: Thierry Neuville – 18 points
  Position 3: Sébastien Ogier – 15 points
  Position 4: Ott Tänak – 12 points

===== CAR PERFORMANCE RATINGS =====
Gravel Car Performance: 423.5
Asphalt Car Performance: 472.0
```
---

## Prerequisites

- Java 11 or higher  
- Maven 3.6+

---
