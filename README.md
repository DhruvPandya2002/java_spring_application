Fruit Billing System

This project is a Java Swing-based billing system designed for fruit billing. It allows the generation of bills, customer management, and product management, and integrates with a MySQL database to store customer and product information. Additionally, it generates bill PDFs using the iText library.

Features

User-friendly billing interface using Java Swing
Stores customer and product data using MySQL
Generates PDF invoices for each bill using iText
Supports product management (add, update, delete)
Supports customer management
Easy to extend and customize

Technologies Used

Java Swing for the graphical user interface (GUI)
MySQL for database management
iText  for generating PDF bills
Apache NetBeans as the recommended IDE

Prerequisites

To run this application, you need to have the following installed:

Java Development Kit (JDK) (version 8 or later)
 [Download JDK](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

Apache NetBeans IDE (version 12 or later)
[Download Apache NetBeans](https://netbeans.apache.org/download/)

MySQL (version 5.7 or later)
[Download MySQL](https://dev.mysql.com/downloads/installer/)

iText library for PDF generation
[Download iText](https://itextpdf.com/en/resources/downloads)

Setup Instructions

Follow the steps below to get the project up and running:

1. Clone the Repository
To get started, clone the repository using Git:

    BASH
    CODE git clone https://github.com/DhruvPandya2002/java_spring_application.git


2. Open the Project in Apache NetBeans
    Open Apache NetBeans and go to File > Open Project
    Select the project directory `fruit_billing_system`.
    The project will load in NetBeans.

3. Configure MySQL Database
    Make sure you have MySQL installed and running.
    Create a new MySQL database and name it `vegetable_shop` (or update the database name in the project configuration as needed).
  
    SQL
        Execute the SQL schema script included in the project (`/db/fruit_billig.sql`) to create the required tables and relationships.
        Update the MySQL connection settings in the project file (usually in a configuration file or within the code where `JDBC` connection details are set):
  
    java
        String url = "jdbc:mysql://localhost:3306/yourproject_name";
        String username = "your_mysql_username";
        String password = "your_mysql_password";

4. Add iText Library to the Project
    Download the iText library from [here](https://itextpdf.com/en/resources/downloads) or use Maven to include it.
    Add the `iText.jar` file to your project's classpath in NetBeans:
      Right-click on the project in NetBeans.
      Select Properties > Libraries > Add JAR/Folder.
      Add the iText.jar file to the classpath.

5. Run the Application
    Once all dependencies are configured, right-click the project in NetBeans and select Run to launch the application.

6. Generate Bills in PDF
    When you create a bill within the application, a PDF file will be generated using the iText library. The file will be saved in the directory specified in the code (you can modify this in the billing form logic).

Troubleshooting

If you encounter issues connecting to the MySQL database, verify that the MySQL service is running and that the connection credentials are correct. If the iText library is not recognized, ensure the JAR is added to the project libraries correctly.


