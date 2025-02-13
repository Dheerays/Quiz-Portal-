

---

# Quiz Portal  

## Overview  
The **Quiz Portal** is a Java-based graphical user interface (GUI) application developed using the **Swing framework**. It allows users to take quizzes dynamically by retrieving questions from a **MySQL database**. The system provides an interactive environment for users to attempt quizzes, view results, and track their performance.  

## Features  
- **User Authentication**:  
  - A login system for users to access the quiz portal.  
- **Dynamic Question Handling**:  
  - Questions are retrieved from a **MySQL database** dynamically.  
  - Questions are presented in a **randomized order** to ensure variety.  
- **Multiple-choice Questions (MCQ)**:  
  - Users can select answers using **radio buttons**.  
  - A **"Next" button** allows progression through the quiz.  
- **Results & Performance Tracking**:  
  - Displays correct and incorrect answers in a tabulated format.  
  - Provides a **detailed explanation** of the user's performance.  
- **Dark-Themed User Interface**:  
  - A visually appealing and **modern GUI design** for an immersive experience.  
- **Modular Code Structure**:  
  - Easy to modify and extend functionality.  

## Technologies Used  
- **Java (Swing for GUI)**  
- **MySQL (for storing quiz questions and user responses)**  
- **JDBC (for database connectivity)**  

## Installation & Setup  

### Prerequisites  
Ensure you have the following installed:  
- **Java Development Kit (JDK) 8 or later**  
- **MySQL Database**  
- **Integrated Development Environment (IDE)** (Eclipse/IntelliJ IDEA/NetBeans)  

### Database Setup  
1. **Create a Database**  
   ```sql
   CREATE DATABASE quiz_portal;
   ```
2. **Use the Database**  
   ```sql
   USE quiz_portal;
   ```
3. **Create a Table for Storing Questions**  
   ```sql
   CREATE TABLE questions (
       Qno INT PRIMARY KEY AUTO_INCREMENT,
       Question TEXT NOT NULL,
       Option_1 VARCHAR(255) NOT NULL,
       Option_2 VARCHAR(255) NOT NULL,
       Option_3 VARCHAR(255) NOT NULL,
       Option_4 VARCHAR(255) NOT NULL,
       Correct_Answer VARCHAR(255) NOT NULL
   );
   ```
4. **Insert Sample Questions**  
   ```sql
   INSERT INTO questions (Question, Option_1, Option_2, Option_3, Option_4, Correct_Answer) 
   VALUES 
   ('What is the capital of India?', 'Mumbai', 'New Delhi', 'Chennai', 'Kolkata', 'New Delhi');
   ```

### Running the Project  
1. Clone the repository:  
   ```sh
   git clone https://github.com/your-repo/quiz-portal.git
   cd quiz-portal
   ```
2. Compile the Java files:  
   ```sh
   javac -d bin -cp .;mysql-connector-java.jar src/GUI/*.java
   ```
3. Run the application:  
   ```sh
   java -cp .;mysql-connector-java.jar GUI.MainApp
   ```

## Project Structure  
```
📂 Quiz Portal  
│── 📂 src  
│   ├── 📂 GUI  
│   │   ├── Login.java         # Handles user authentication  
│   │   ├── Choice.java        # Displays quiz categories  
│   │   ├── Question.java      # Loads quiz questions dynamically  
│   │   ├── Result.java        # Displays quiz results  
│   │── 📂 Database  
│   │   ├── Connection.java    # Manages database connectivity  
│── 📂 resources  
│   ├── quiz_data.sql          # SQL dump for database setup  
│── README.md  
```

## How It Works  
1. **Login**: Users enter their credentials to access the quiz portal.  
2. **Quiz Selection**: Users can choose a quiz category.  
3. **Answering Questions**:  
   - The system fetches questions from the database.  
   - Users select an answer and click "Next" to proceed.  
4. **Result Calculation**:  
   - The system evaluates the answers and displays the result.  
   - A performance breakdown is shown in a **tabulated format**.  

## Future Enhancements  
- **User Registration System** for personalized quiz attempts.  
- **Timer Functionality** to limit the time per question.  
- **Leaderboard System** to rank users based on performance.  
- **Exportable Reports** for users to review their results offline.  

## Author  
**Shakti Dheerays S**  
  

---
