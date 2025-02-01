---
lab:
    title: 'Exercise - Create classes and objects in C#'
    module: 'Get started with classes and objects in C#'
---


# Create classes and objects in CSharp

In this exercise, you create a console app that uses class definitions to instantiate objects using the `new` operator.

This exercise includes the following tasks:

- Create a console app and a class file for the `Person` class
- Create additional constructors for the `Person` class
- Implement instance and static constructors

This exercise should take approximately **15** minutes to complete.

## Before you start

Before you can start this exercise, you will need to...

1. Ensure that you have the latest LTS version of the .NET SDK installed on your computer. You can download the latest version of the .NET SDK from the following URL: [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
1. Ensure that you have Visual Studio Code installed on your computer. You can download Visual Studio Code from the following URL: [https://code.visualstudio.com/](https://code.visualstudio.com/)
1. Ensure that you have the C# Dev Kit configured in Visual Studio Code.

For addition help configuring the Visual Studio Code environment, see [https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/](https://learn.microsoft.com/en-us/training/modules/install-configure-visual-studio-code/)

## Task 1: Create a console app and a class file for the `Person` class

Use the following steps to complete this section of the exercise:

1. Open Visual Studio Code.

1. Use Visual Studio Code to create a folder named `MyClassProjects` on the Windows Desktop.

1. Use the Command Palette to create a new console app named `Classes_M1`.

1. Open the Program.cs file and delete the default “hello, world” code.

1. Use the Command Palette to create a class named `Person`

1. Notice that a namespace is specified.

1. Add a default constructor to the `Person` class.

1. Add local variables (`firstName`, `lastName`) to the constructor and a `Console.WriteLine()` statement announcing that an instance of the `Person` class has been instantiated using the default name values. Show the name as well.

1. Switch to the Program.cs file

1. Create a using statement for the namespace specified in the `Person` class.

1. Create an instance of the `Person` class in the Program.cs file.

1. Run the app.

## Task 2: Create additional constructors for the Person class

Use the following steps to complete this section of the exercise:

1. Open the Person.cs file

1. Add a second constructor that accepts a first name parameter.

1. Add local variables to the constructor, assigning the value that’s passed into the constructor to the first name.

1. Update the Console.WriteLine() message.

1. Switch to the Program.cs file

1. Create a string variable named firstName. Assign a value of “Jane” to firstName.

1. Create a second instance of the Person class that uses the new constructor.

1. Run the app

1. In the Person.cs file, add a third constructor that accepts first and last names.

1. Add local variables to the constructor, assigning the values that are passed into the constructor to the first and last name variables.

1. In the Program.cs file, create a third instance of the Person class that uses the new constructor.

1. Run the app

## Task 3: Implement instance and static constructors

Use the following steps to complete this section of the exercise:

1. In the Person.cs file, ...

## Clean up

<!-- Good practice - especially as self-paced learners will be using their own subscriptions -->
<!-- Delete this section if it is not needed -->

Now that you've finished the exercise, you should ...

1. Step 1
2. etc.
