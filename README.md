# Welcome to your organization's demo respository
This code repository (or "repo") is designed to demonstrate the best GitHub has to offer with the least amount of noise.

The repo includes an `index.html` file (so it can render a web page), two GitHub Actions workflows, and a CSS stylesheet dependency.

# GeoQuester

## Domain Model

### Overview
GeoQuester is designed to intertwine physical activity with interactive challenges, encouraging exploration and fitness through a gamified environment. Our app integrates users, challenges, and tasks into a cohesive system where users can engage in various location-based challenges to earn rewards and track their progress.

### Entities

#### User
- **Attributes:**
  - `ID`: Unique identifier, String
  - `Username`: String
  - `Email`: Unique, String
  - `Password`: Encrypted, String
  - `Location`: String
  - `Profile Picture`: URL, String
  - `Total Steps`: Number, cumulative steps count
  - `Challenges Completed`: Array of Challenge IDs

#### Challenge
- **Attributes:**
  - `ID`: Unique identifier, String
  - `Title`: String
  - `Description`: Text, String
  - `Location`: String, relevant to the challenge
  - `Tasks`: Array of Task Objects

#### Task
- **Attributes:**
  - `ID`: Unique identifier, String
  - `Description`: String
  - `Proof of Completion`: URL, String
  - `Points`: Number, awarded upon completion

### Relationships
- **User to Challenge**: Many-to-Many
  - Users can join multiple challenges.
  - Challenges can have multiple participants.
- **User to Task**: One-to-Many
  - Users complete multiple tasks within challenges.
- **Challenge to Task**: One-to-Many
  - Each challenge includes several specific tasks.

### Domain Model Diagram
This diagram visualizes the relationships and entity connections within GeoQuester: 
![image](https://github.com/Innova-Tech-Labs/demo-repository/assets/146989043/ee953aa6-6144-4b9c-9815-ccc5462e403e)



