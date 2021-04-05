# Basic MongoDB Commands

### **Description:**
> ***get a list of commands.***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db.help()
```
----------------------------------------

### **Description:**
> ***print a list of all databases on the server.***
---------------------------------------

<strong>Command: </strong>

```MongoDB
show dbs
```
----------------------------------------

### **Description:**
> ***create new database "myTestDB".***
---------------------------------------

<strong>Command: </strong>

```MongoDB
use myTestDB
```
----------------------------------------
### **Description:**
> ***know your current selected database.***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db
```
----------------------------------------

### **Description:**
> ***drop the current selected database.***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db.dropDatabase()
```
----------------------------------------

### **Description:**
> ***create new collection "Employee".***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db.createCollection("Employee")
```
----------------------------------------
### **Description:**
> ***print a list of all collections created.***
---------------------------------------

<strong>Command: </strong>

```MongoDB
show collections
```
----------------------------------------

### **Description:**
> ***drop the collection "Employee".***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db.Employee.drop()
```
----------------------------------------

### **Description:**
> ***insert document in collection "Employee".***
---------------------------------------

<strong>Command: </strong>

```MongoDB
db.Employee.insert({name: 'Raj', address: 'Bangalore'})
```
----------------------------------------
