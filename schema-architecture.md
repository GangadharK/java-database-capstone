Section 1: Architecture Summary – The current smart clinic architecture consist of three layers 
1- application layer handles by thyme leaf and REST API end points 
2- Service Layer or business lyer is implemented by Thyme leaf controller and REST controller in spring boot, One is used to serve the html view dashboards for admin and doctor and REST controller for patient details management
3- Data base layer :  which is handled by 2 types of databases
    1: my sql for storing regular transactional data user info and login
    2: Mongo DB for storing precriptions and other complicated datawhich doesnt have fixed format
Section 2:
    a: Dashboards Flow ( Admin, Doctor)
        1- Dash board connects with Thymeleaf controller 
        2- Thymelef connects with Service layer where data validation occurs
        3- Repository/ DTO layer: service layer connects to repo which inturn connects with MYSQL models and access data stored and manage
        4- The store date is either viewed or updated and response is returned to Thymeleaf controller which deisplays the web view
    b: REST Models (Appointment, Patient Dashboard, Patient Record)
        1- Through Provided endpoints either web layer or other tolls connect to Rest controller
        2- Rest Controller connects with Service layer where Input data is validated
        3- which connects with either MYsql or Mongo DB repository
        4- Mongo DB repo connects with mongo DB database and Models
        5- which is used to update the data or view the data


