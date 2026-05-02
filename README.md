# 🚗 Vehicle Hibernate Maven Project

This project demonstrates how to use **Hibernate ORM with Maven** to perform basic database operations on a `Vehicle` entity.

---

## 📌 Project Overview

The application performs the following operations:

* ✅ Insert a new Vehicle record
* ✅ Update Vehicle details (Name, Status) using ID

It uses:

* Hibernate ORM (JPA Annotations)
* Maven for dependency management
* MySQL database (`fsadendexam`)

---

##Project Structure

```
VehicleHibernateProject
 ├── src/main/java/com/klef/fsad/exam
 │    ├── Vehicle.java
 │    └── ClientDemo.java
 ├── src/main/resources
 │    └── hibernate.cfg.xml
 └── pom.xml
```

---

##Technologies Used

* Java
* Hibernate ORM
* Maven
* MySQL
* JPA (Java Persistence API)

---

##Entity: Vehicle

The `Vehicle` class contains the following attributes:

| Field       | Type   | Description                |
| ----------- | ------ | -------------------------- |
| id          | int    | Auto-generated primary key |
| name        | String | Vehicle name               |
| description | String | Vehicle description        |
| date        | Date   | Created/updated date       |
| status      | String | Availability status        |

---

##Database Configuration

Database Name: **fsadendexam**

### Create Database

```sql
CREATE DATABASE fsadendexam;
USE fsadendexam;
```

---

##Hibernate Configuration

Update your database credentials in:

```
src/main/resources/hibernate.cfg.xml
```

```xml
<property name="hibernate.connection.username">root</property>
<property name="hibernate.connection.password">password</property>
```

---

##How to Run

1. Clone the repository:

```bash
git clone https://github.com/your-username/VehicleHibernateProject.git
```

2. Open in IDE (IntelliJ / Eclipse)

3. Update MySQL credentials in `hibernate.cfg.xml`

4. Run:

```
ClientDemo.java
```

---

##Operations Explained

### 1. Insert Operation

* Creates a new `Vehicle` object
* Saves it using `session.save()`
* ID is auto-generated

### 2. Update Operation

* Fetches vehicle using ID
* Updates fields (`name`, `status`)
* Saves changes using `session.update()`

##Sample Output

```
Vehicle Inserted with ID: 1
Vehicle Updated Successfully
```

---

Notes

* Hibernate automatically creates the `vehicle` table
* Make sure MySQL server is running
* Ensure correct dependency versions in `pom.xml`

---

##Author

* 2400031294
* Course: FSAD
* Package: `com.klef.fsad.exam`

---

##License

This project is for educational purposes.
