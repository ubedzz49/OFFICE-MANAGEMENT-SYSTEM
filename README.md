# OFFICE-MANAGEMENT-SYSTEM
OOP based c++ project


#### **Overview**
The **Office Management System (OMS)** is a C++ program designed to simulate the management of employees, tasks, and communication within an office environment. The system is built using Object-Oriented Programming (OOP) principles, making it modular, scalable, and easy to maintain. It allows employees to manage tasks, communicate with subordinates, and handle administrative tasks like salary crediting, team management, and employee rewards.


### **Key Features**

1. **Employee Management**
   - **Employee Class**: Represents an employee with attributes like `id`, `name`, `designation`, `salary`, `account balance`, `score`, and `messages`.
   - **Hierarchy**: Employees can have subordinates, forming a hierarchical structure.
   - **Login System**: Employees can log in using their `id` and `password`.
   - **Add/Remove Subordinates**: Admins can add or remove employees from teams.
   - **Employee of the Month**: Employees are rewarded based on their performance (task completion).

2. **Task Management**
   - **Task Class**: Represents a task with attributes like `id`, `heading`, `description`, and `priority`.
   - **Task Assignment**: Tasks can be assigned to employees or their subordinates.
   - **Task Completion**: Employees can mark tasks as completed, which updates their score.
   - **Task Quitting**: Employees can quit tasks, which are then reassigned to their supervisor.

3. **Communication**
   - **Messaging**: Employees can send messages to their subordinates or specific designations.
   - **Complaints**: Employees can send complaints to their supervisors.

4. **Salary Management**
   - **Salary Crediting**: Admins can credit salaries to employees from a central fund.
   - **Account Balance**: Employees can view their account balance.

5. **Admin Dashboard**
   - **Team Management**: Admins can view the full team hierarchy, add/remove employees, and manage free employees (those not in any team).
   - **Fund Management**: Admins can view and manage the available fund for salary crediting.
   - **Month-End Operations**: Admins can end the month, reset scores, and reward the best-performing employees.

6. **User Interface**
   - **Console-Based Interface**: A simple console-based interface allows users to interact with the system.


### **Implementation Details (Focusing on OOP)**

1. **Classes and Objects**
   - **`task` Class**: Represents a task with attributes like `id`, `heading`, `desc`, and `priority`. It uses a constructor to initialize these attributes.
   - **`employee` Class**: Represents an employee with attributes like `id`, `name`, `designation`, `salary`, `subordinates`, and `tasks`. It also includes methods for task management, communication, and salary handling.
   - **`comparetask` Struct**: A comparator for prioritizing tasks based on their priority.

2. **Encapsulation**
   - All attributes of the `task` and `employee` classes are private, and access is controlled through public methods. For example, `viewmessages()`, `viewaccbal()`, and `addsub()` are methods that provide controlled access to private data.

3. **Abstraction**
   - The `employee` class abstracts the complexity of managing tasks, subordinates, and communication. Users interact with high-level methods like `assigntask()`, `viewmessages()`, and `creditsalary()` without needing to know the internal implementation.

4. **Data Structures**
   - **`priority_queue`**: Used to manage tasks based on their priority.
   - **`vector`**: Used to store subordinates and messages.
   - **`unordered_map`**: Used to store employee records and free employees.

5. **Error Handling**
   - Basic error handling is implemented, such as checking for valid credentials during login and ensuring sufficient funds for salary crediting.

