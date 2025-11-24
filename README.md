# Inventory Management System

## 1. Project Overview
This is an Inventory Management System built as a GUI desktop application developed in **Java** using **MySQL** for database management. The interface was designed using **Swing** and database connectivity is handled via the **JDBC API**.

This application is designed for small to mid-sized retail stores to digitize their processes. It allows business owners to easily maintain and manage an inventory of products, customers, suppliers, users, and sales transactions.

## 2. Features
**User Management:**
* **Role-Based Access:** Supports two user types: **Administrator** and **Employee**.
* **Admin Privileges:** Admins can manage all personnel and view user logs (login/logout times).
* **Security:** Secure login verification against the database.

**Inventory & Stock Control:**
* **CRUD Operations:** Users can Add, Edit, and Delete products, suppliers, and customers.
* **Real-time Stock Updates:** Any transaction made (Sale or Purchase) automatically updates the stock availability in the inventory.
* **Current Stock View:** A dedicated section to check the availability of every item.

**Transaction Management:**
* **Sales Module:** Users only need to enter the `Product Code`; the system automatically retrieves details (price, name) and calculates the bill.
* **Purchase Module:** Logs new stock purchases and updates inventory counts immediately.
* **Search Functionality:** Each section includes a search bar to filter data quickly.

## 3. Technologies & Tools Used
* **Language:** Java (JDK 16)
* **GUI Framework:** Java Swing
* **Database:** MySQL Server
* **Database Connectivity:** JDBC API
* **IDE Tools:** JetBrains IntelliJ IDE / Apache NetBeans (for GUI design)
* **Database Tool:** MySQL Workbench

## 4. Steps to Install & Run
**Prerequisites:** Ensure you have **JDK 16 (or higher)** and **MySQL Server** installed.

1.  **Download the Source:**
    * Download and unzip the project folder.
2.  **Database Setup:**
    * Open **MySQL Workbench**.
    * Import the SQL dump file included in the project folder to create the local schema and tables.
3.  **Configure Credentials:**
    * *Default credentials are `root` / `root`.*
    * If your MySQL password differs, go to the `lib` folder and open `DBCredentials.xml`.
    * Edit lines 12 and 13 to match your local database settings:
        ```xml
        <entry key="username">YOUR_USERNAME</entry>
        <entry key="password">YOUR_PASSWORD</entry>
        ```
4.  **Run the Application:**
    * Execute the `InventoryManagement.jar` file located in the folder.

## 5. Instructions for Testing
To verify the system functionalities, follow this workflow:

1.  **Login Test:**
    * Launch the app.
    * Enter Username: `root`, Password: `root`.
    * *Expected Result:* You should be directed to the Dashboard.
2.  **Add Product Test:**
    * Navigate to the **Products** section.
    * Click "Add" and enter dummy product details (e.g., "Test Item", Price: 100).
    * *Expected Result:* The item appears in the table.
3.  **Sales Transaction Test:**
    * Go to the **Sales** section.
    * Enter the Customer ID and the Product Code of the item you just added.
    * Complete the transaction.
    * *Expected Result:* The **Current Stock** count for that item should decrease by 1.
4.  **Admin Log Test:**
    * Go to the **User Logs** section (Admin only).
    * *Expected Result:* You should see a record of your current login session.

## 6. Project Screenshots

### Login Page

The login page takes in the credentials entered by the user and verifies with the database.

![loginpage](screenshots/login.png)

### Dashboard/Welcome Page

The landing page of the application after a successful login.

![welcome](screenshots/welcome.png)

### Products

The products section allows the user to add, edit and delete products from the store's inventory.

![products](screenshots/products.png)

### Current Stock

This section allows the user to check the availability of every item.

![stock](screenshots/stock.png)

### Suppliers

Here, the user can manage and manipulate the record of all the suppliers associated with the store.

![suppliers](screenshots/suppliers.png)

### Customers

Allows user to add new customers or update/delete existing customers in the database.

![customers](screenshots/customers.png)

### Sales

This section is where users can sell a product and manage all the sales transactions. 
The user only needs to enter the customer and product code and the software will handle the rest, showing all the necessary details like available stock and selling price of the product. 

![sales](screenshots/sales.png)

### Purchase

This section is where users can view purchase logs and enter new purchase transactions. Similar to the sales section, this section only requires the user to enter the product code and the details that are already available in the database will immediately be displayed in the respective spaces.

![purchase](screenshots/purchase.png)

### Users

This section is only available to **ADMINISTRATORS**. It allows them to view, add and delete any users.

![users](screenshots/users.png)

### User Logs

Stores and shows the administrator a log of all the users that have previously logged in, including their login time and logout time.

![logs](screenshots/logs.png)

***

## Technologies Used

The following are the technologies that have been used in the development of this project. All of them are free to use.
  - JetBrains IntelliJ IDE
  - Apache NetBeans IDE (for the GUI designer)
  - MySQL Server and Workbench
  - JDK 16

## ER Diagram

The ER diagram for the sample schema that has been used in the application.

![erdiag](screenshots/ERDiagram.png)

## Source Code

The software code has been divided into four different packages:
  - Data Access Object (DAO): Contains the data access layer of the software that interacts directly with the database and its tables. Used for retrieval and modification of data.
  - Data Transfer Object (DTO): Contains the data transfer layer that allows the data to be transferred between the data access layer and the UI layer.
  - Database: Contains the ConnectionFactory class that retrieves the database connection and verifies user credentials for the application.
  - User Interface (UI): Contains all the GUI classes making up the interface layer of the software.

Click [here](src/com/inventory/) to skip directly to the source code.

# Inventory-Management-System
Developed using Java and MySQL, this system replaces inefficient manual tracking methods with a centralized platform for managing inventory, processing sales transactions, and maintaining supplier records. It features a user-friendly GUI built with Java Swing, providing secure, role-based access and real-time visibility into stock levels.

