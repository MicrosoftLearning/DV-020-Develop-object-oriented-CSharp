---
lab:
    title: 'Exercise - Create classes and objects in C#'
    module: 'Get started with classes and objects in C#'
---


# Create classes and objects in CSharp

Classes are the building blocks of object-oriented programming in C#. In this exercise, you create a console app that uses class definitions to instantiate objects using the `new` operator.

This exercise takes approximately **15** minutes to complete.

## Before you start

Before you can start this exercise, you need to:

1. Ensure that you have the latest LTS version of the .NET SDK installed on your computer. You can download the latest versions of the .NET SDK using the following URL: [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
1. Ensure that you have Visual Studio Code installed on your computer. You can download Visual Studio Code using the following URL: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
1. Ensure that you have the C# Dev Kit configured in Visual Studio Code.

For addition help configuring the Visual Studio Code environment, see [Install and configure Visual Studio Code for C# development](https://learn.microsoft.com/training/modules/install-configure-visual-studio-code/)

## Exercise scenario

Suppose you're helping a non-profit company with a software project. You have experience creating structured apps in C#, but no experience with object-oriented programming. You need to gain experience before starting work on the company software. You decide to create a simple banking app that includes `Customer` and `Account` classes.

This exercise includes the following tasks:

1. Create a console app and `Customer` class

1. Create instance constructors for the `Customer` class

1. Create an `Account` class with instance constructors

1. Implement static constructors for the `Account` class

## Task 1: Create a console app and `Customer` class

In this task, you create a console app, add a `Customer` class to the project, and then create class definition for the `Customer` class that includes public fields and a parameterless constructor.

Use the following steps to complete this section of the exercise:

1. Open Visual Studio Code.

1. Use Visual Studio Code to create a folder named `MyClassProjects` on the Windows Desktop.

1. Use the Command Palette to create a new console app named `Classes_M1`.

1. Open the Program.cs file and delete the default “hello, world” code.

1. Use the Command Palette to create a class named `Customer`

1. Notice that a namespace is specified.

1. Add a default constructor to the `Customer` class.

1. Add local variables (`firstName`, `lastName`) to the constructor and a `Console.WriteLine()` statement announcing that an instance of the `Customer` class has been instantiated using the default name values. Show the name as well.

1. Switch to the Program.cs file

1. Create a using statement for the namespace specified in the `Customer` class.

1. Create an instance of the `Customer` class in the Program.cs file.

1. Take a minute to review your code.

    ```csharp

    
    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Task 2: Create instance constructors for the `Customer` class

In this task, you create additional instance constructors for the `Customer` class that accept parameters for the first name, last name, and account number.

Use the following steps to complete this section of the exercise:

1. Open the Customer.cs file

1. Add a second constructor that accepts parameters for the customers first and last name.

1. Add local variables to the constructor, assigning the values passed into the constructor.

1. Update the `Console.WriteLine()` message to include the customer name.

1. Switch to the Program.cs file

1. Create a string variable named `firstName`. Assign a value of “Jane” to `firstName`.

1. Create a second instance of the Customer class that uses the new constructor.

1. Run the app

1. In the Customer.cs file, add a third constructor that accepts first and last names.

1. Add local variables to the constructor, assigning the values that are passed into the constructor to the first and last name variables.

1. In the Program.cs file, create a third instance of the Customer class that uses the new constructor.

1. Take a minute to review your code.

    ```csharp

    
    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Task 3: Create an `Account` class with instance constructors

In this task, you create an `Account` class that includes instance constructors that accept parameters for the account number, account type, and balance.

Use the following steps to complete this section of the exercise:

1. Use the Command Palette to create a class named `Account`.

1. next step

1. next step

1. next step

1. Take a minute to review your code.

    ```csharp

    
    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Task 4: Implement static constructors for the `Account` class

In this task, you create a static constructor for the `Account` class that initializes a static field.

Use the following steps to complete this section of the exercise:

1. In the Account.cs file, ...

1. next step

1. next step

1. next step

1. Take a minute to review your code.

    ```csharp

    
    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Clean up

<!-- Good practice - especially as self-paced learners will be using their own subscriptions -->
<!-- Delete this section if it is not needed -->

Now that you've finished the exercise, you should ...

1. Step 1
2. etc.
