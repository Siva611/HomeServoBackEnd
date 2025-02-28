
# Hi, I'm Siva 👋


#  Home Servo Application 🌟

- This application will used as a __Home Service Management__ platform that connects customers with service vendors for various home repair and maintenance tasks.
The system allows customers to request services, track work progress, and make payments, while vendors can manage their work and Generate Automated Cost Estimates. 

<br>


#  Technologies 🛠️


## 🖥️ Backend:
<img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg"/><img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg"/>

**IDE:**  
<img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/eclipse/eclipse-original.svg"/>


- Technologies: **Java, Spring Boot** <br>
- IDE: **Eclipse**  


---

## 🗄️ Database:
<img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg"/>

**IDE:** 

<img width="50px" src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg"/>


- Technology: **MySQL** <br>
- Tool: **MySQL Workbench**  

---

## 🛠️ APIS Testing Tool

For testing the APIs, we are using Postman.

**IDE:**  

<img width="50px" src="https://www.svgrepo.com/show/354202/postman-icon.svg"/>

---

## 🔹 Description
- HomeServo is a smart home service management system that integrates backend, and database technologies to provide seamless automation and control.

## 🔹 Features
- Secure backend 🛠️ API with Spring Boot
- MySQL database integration

<br>


# Features 🚀

## 🔹Customer Portal

- **User Registration & Login:**   
  - Customers can register and log in securely.

- **Profile Management:**    
  - Customers can update and manage their details. 

- **Service Requests:**    
  - Users can select repair work based on the type of issue.  

- **Automated Cost Estimation:**  
  - Once the vendor Starts and Ends the work, an estimated cost is generated. 

- **Secure Payments:**  
  - Customers can make payments after the service is completed.

<br>

## 🔹 Vendor Portal 

- **Vendor Registration & Login:**  
  -  Vendors can sign up and log in to their accounts.

- **Service Management:**  
  -  Vendors can view assigned service requests.
- **Work Status Updates:**  
  - Vendors can start and complete tasks, triggering automatic cost estimation.

- **Work Tracking:**  
  - Vendors can view the status of Ongoing work.

- **Payment Validation:**  
  - Customers validate the cost and complete the payment.

--- 

# Installation 🔧


## Backend Setup

### 1. Clone the backend repository:

- git clone https://github.com/Siva611/HomeServoBackEnd <br>
- cd homeservo-backend

## 🔹 Database Configuration  

To configure the Update the MySQL database in **Spring Boot**, add the following properties in `application.properties`:  

```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/your_database_name
    spring.datasource.username=your_username
    spring.datasource.password=your_password
```


### Note: 
- Change the database name (__*your_database_name*__) if needed.
Ensure MySQL is running and the database is created.


### 3. Build and run the backend:

- mvn clean install <br>
- mvn spring-boot:run


<br> 


# 🛠️ API 


## 🔹 Customer API Endpoints  

<br>

### **Register New Customer :**  
- **Method:** `POST`  
- 🛠️**API URL:** `http://localhost:8080/customers/ `  
- **Content-Type:** `application/json`  
- **Request Body:**  
  ```json
  {
        "name": "Custmers3",
        "email": "cust@gmail.com",
        "password": "Cus@12345",
        "phone": 7788445599,
        "familyCount": 6,
        "address": {
            "d_No": "122",
            "street": "VenStreet",
            "landMark": "Kgt",
            "district": "venDist",
            "state": "ve",
            "pincode": 774455
        }
    }
  ```


### **Login Customer :**  
- **Method:** `GET`  
- 🛠️**API URL:** `http://localhost:8080/customers/login?email=cust@gmail.com&password=Cus@12345`  
- **Content-Type:** `application/json`


### **Get Customer By ID :**  
- **Method:** `GET`  
- 🛠️**API URL:** `http://localhost:8080/customers/1`  
- **Content-Type:** `application/json`  


### **Update Customer :**  
- **Method:** `PUT`  
-  🛠️**API URL:** ` http://localhost:8080/customers/`  
- **Content-Type:** `application/json`  
- **Request Body:**  
  ```json
  {
    "id": 3,
        "name": "Custmers3",
        "email": "cust@gmail.com",
        "password": "Cus@12345",
        "phone": 7788445599,
        "familyCount": 6,
        "address": {
            "id": 8,
            "d_No": "122",
            "street": "VenStreet",
            "landMark": "Kgt",
            "district": "venDist",
            "state": "ve",
            "pincode": 774455
        }
    }
 
 
### **Delete Customer :**  
- **Method:** `DELETE`  
-🛠️ **API URL:** `http://localhost:8080/customers/1`  
- **Content-Type:** `application/json`  

---
<br>

## 🔹 Vendor API Endpoints  

<br>

### **Register New Vendor :**  
- **Method:** `POST`  
- 🛠️**API URL:** `http://localhost:8080/vendors`  
- **Content-Type:** `application/json`  
- **Request Body:**  
  ```json
  {
    "name": "Vendornew",
    "email": "vendor22@gmail.com",
    "password": "Ven@12345",
    "phoneNo": 7788445599,
    "costPerDay": "12345",
    "role": "super",
    "familyCount": 6,
    "address": {
      "d_No": "122",
      "street": "VenStreet",
      "landMark": "Kgt",
      "district": "venDist",
      "state": "ve",
      "pincode": 774455
    }
  }
  ```

### **Login Vendor :**  
- **Method:** `GET`  
- 🛠️**API URL:** `http://localhost:8080/vendors/login?email=vendor22@gmail.com&password=Ven@12345`  
- **Content-Type:** `application/json`  

### **Get Vendor By ID :**  
- **Method:** `GET`  
- 🛠️**API URL:** `http://localhost:8080/vendors/1`  
- **Content-Type:** `application/json`  

### **Update Vendor :**  
- **Method:** `PUT`  
- 🛠️**API URL:** `http://localhost:8080/vendors`  
- **Content-Type:** `application/json`  
- **Request Body:**  
  ```json
  {
    "id": 3,
    "name": "Vendornew",
    "email": "vendor22@gmail.com",
    "password": "Ven@12345",
    "phoneNo": 7788445599,
    "costPerDay": "12345",
    "role": "super",
    "familyCount": 6,
    "address": {
      "id": 9,
      "d_No": "122",
      "street": "VenStreet",
      "landMark": "Kgt",
      "district": "venDist",
      "state": "ve",
      "pincode": 774455
    }
  }
  ```

### **Delete Vendor :**  
- **Method:** `DELETE`  
- 🛠️**API URL:** `http://localhost:8080/vendors/3`  
- **Content-Type:** `application/json`  
