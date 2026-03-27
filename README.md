

#  Universe Database (SQL) – freeCodeCamp Project

This project is a relational database built as part of the **freeCodeCamp Relational Database Certification**. It models a simplified universe containing galaxies, stars, planets, and moons, demonstrating strong SQL fundamentals and database design principles.

---

## 🚀 Project Overview

The **Universe Database** is designed to represent astronomical structures using relational tables and constraints. It showcases how different celestial bodies are connected through relationships like:

* A galaxy contains many stars
* A star can have multiple planets
* A planet can have multiple moons

---

## 🛠️ Technologies Used

* **SQL (PostgreSQL)**
* **psql (Command Line Tool)**
* **Relational Database Concepts**

---

## 📂 Database Structure

The database consists of the following main tables:

### 🌌 Galaxy

Stores information about galaxies.

* `galaxy_id` (Primary Key)
* `name` (Unique)
* `type`
* `distance_from_earth`

---

### ⭐ Star

Stores stars and links them to galaxies.

* `star_id` (Primary Key)
* `name` (Unique)
* `galaxy_id` (Foreign Key)
* `age`
* `is_spherical`

---

### 🪐 Planet

Represents planets orbiting stars.

* `planet_id` (Primary Key)
* `name` (Unique)
* `star_id` (Foreign Key)
* `has_life`
* `planet_type`

---

### 🌙 Moon

Represents moons orbiting planets.

* `moon_id` (Primary Key)
* `name` (Unique)
* `planet_id` (Foreign Key)
* `is_spherical`

---

### 🛰️ Additional Table (Optional)

You may also include:

* `description` table or extra metadata table depending on your implementation

---

## 🔗 Relationships

* One **galaxy** → Many **stars**
* One **star** → Many **planets**
* One **planet** → Many **moons**

---

## 📊 Key Features

* ✅ Proper use of **Primary Keys & Foreign Keys**
* ✅ Enforced **UNIQUE constraints**
* ✅ Use of **NOT NULL constraints**
* ✅ Logical relational structure
* ✅ Clean and normalized schema design

---

## ⚙️ How to Run the Project

1. **Install PostgreSQL**

2. **Open psql and create database**

```sql
CREATE DATABASE universe;
```

3. **Connect to database**

```sql
\c universe
```

4. **Import the SQL file**

```bash
psql -U your_username -d universe -f universe.sql
```

---

## 🧪 Example Queries

```sql
-- Get all planets with life
SELECT * FROM planet WHERE has_life = true;

-- List all moons of a planet
SELECT name FROM moon WHERE planet_id = 1;

-- Join planets with their stars
SELECT planet.name, star.name
FROM planet
JOIN star ON planet.star_id = star.star_id;
```

---

## 🎯 Learning Outcomes

Through this project, I learned:

* Relational database design
* Writing complex SQL queries
* Table relationships and normalization
* Data integrity using constraints
* PostgreSQL database management

---

## 📸 Project Source

Built as part of the **freeCodeCamp Relational Database Certification**

---

## 📈 Future Improvements

* Add more astronomical data fields
* Create stored procedures
* Build a frontend to visualize the database
* Add indexing for performance optimization

---

## 🤝 Contributing

This is a learning project, but suggestions and improvements are welcome!

---

## 📄 License

This project is open-source and available under the **MIT License**.

---

## 👨‍💻 Author

Built by **mipresh
On my journey to becoming a full-stack developer

