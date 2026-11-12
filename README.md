# Distributed Hotel Management System: Admin Web Panel

The staff and admin web panel of a three-part restaurant automation system. Managers run the menu, tables, orders, billing and promotions, and the Android table app and its API read the same MySQL database.

| Part | Repo |
|---|---|
| **Admin web panel (this repo)** | Distributed-Hotel-Management-System-Web |
| Mobile API | [Distributed-Hotel-Management-System-API](https://github.com/Paradox2405/Distributed-Hotel-Management-System-API) |
| Android table app | [Distributed-Hotel-Management-System-App](https://github.com/Paradox2405/Distributed-Hotel-Management-System-App) |

## Features

- Staff login and registration
- **Menu management**: categories, dishes, ingredients and units
- **Tables**, **taxes** and **orders**
- **Billing**
- **Call-waiter** requests from tables
- Customer **feedback**
- **Ads** and greetings shown on the table app
- Dashboard **charts** (Flot)

## Tech stack

- **Java EE**: servlets with an MVC split (controllers, DAOs, entities) and JSP views
- **MySQL** over JDBC
- **Apache Tomcat**
- jQuery admin theme (DataTables, Flot charts, form widgets)

## Project structure

```
src/com/comsats/restauto/
  controller/   Authentication, Billing, CallWaiter, Chart, Dish, Feedback,
                Ingredient, Order, Register, Table, Tax, Unit, Ads, Greeting
  dao/          one DAO per table
  entity/ servlet/ util/ constVar/
WebContent/     login.jsp, admin pages, js/ css/ (admin theme)
```

## Running

1. Import into Eclipse (Dynamic Web Project) or IntelliJ with Tomcat.
2. Create the MySQL database and set the JDBC connection details.
3. Deploy to Tomcat and open `http://localhost:8080/RestAutomationAdmin/`.
