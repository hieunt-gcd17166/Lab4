# Lab4
This is a Tutorial: Get Started with Entity Framework 6 Code First using MVC 5

- In this series you will learn how to build an ASP.NET MVC 5 application that uses Entity Framework 6 for data access.
- This tutorial uses the Code First workflow. For information about how to choose between Code First, Database First, and Model First
- In this Tutorial:
  - Create an MVC web app
  - Set up the site style
  - Install Entity Framework 6
  - Create the data model
  - Create the database context
  - Initialize DB with test data
  - Set up EF 6 to use LocalDB
  - Create controller and views
  - View the database
# BODY
Create an MVC web app.
In New ASP.NET Web Application - ContosoUniversity, select MVC.
- Set up the site style in the Layout.cshtml file with the path is: "Views\Shared_Layout.cshtml" and make some changes
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/Layout.PNG)
- Replace the contents of the file with the following code to replace the text about ASP.NET and MVC with text about this application:
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/ViewIndex.PNG)
- Next you'll create entity classes for the Contoso University application. You'll start with the following three entities:
  - Student
  - Enrollment
  - Course

- Student Class
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/StudentClass.PNG)
- Enrollment Class
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/EnrollmentClass.PNG)
- Course Class
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/CourseClass.PNG)

We'll say more about the DatabaseGeneratedAttribute attribute in a later tutorial in this series. Basically, this attribute lets you enter the primary key for the course rather than having the database generate it.

--The main class that coordinates Entity Framework functionality for a given data model is the database context class. You create this class by deriving from the System.Data.Entity.DbContext class. In your code, you specify which entities are included in the data model. You can also customize certain Entity Framework behavior. In this project, the class is named SchoolContext.

--Name the new folder DAL (for Data Access Layer). In that folder, create a new class file named SchoolContext.cs, and replace the template code with the following code:
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/SchoolContext.PNG)

--And then, initialized database with the test data. Particularly, created a new class named SchoolInitializer.cs and create the database with some test data: 
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/DataSchool.PNG)
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/Data2.PNG)

--To tell Entity Framework to use my initializer class, I added an element to the entityFramework element in the application Web.config file: 
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/ConnectString.PNG)

# Result 
And now let's see a result
![add text](https://github.com/hieunt-gcd17166/Lab4/blob/master/ContosoUniversity/img/Demo1.gif)
