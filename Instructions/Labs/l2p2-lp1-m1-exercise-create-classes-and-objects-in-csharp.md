---
lab:
    title: 'Exercise - Create classes and objects in C#'
    module: 'Get started with classes and objects in C#'
---


# Create classes and objects in C#

Classes are the building blocks of object-oriented programming. In this exercise, you create a console app that uses class definitions to instantiate objects using the `new` operator.

This exercise takes approximately **15** minutes to complete.

## Before you start

Before you can start this exercise, you need to:

1. Ensure that you have the latest LTS version of the .NET SDK installed on your computer. You can download the latest versions of the .NET SDK using the following URL: [https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)
1. Ensure that you have Visual Studio Code installed on your computer. You can download Visual Studio Code using the following URL: [https://code.visualstudio.com/download](https://code.visualstudio.com/download)
1. Ensure that you have the C# Dev Kit configured in Visual Studio Code.

For addition help configuring the Visual Studio Code environment, see [Install and configure Visual Studio Code for C# development](https://learn.microsoft.com/training/modules/install-configure-visual-studio-code/)

## Exercise scenario

Suppose you're helping a non-profit company with a software project. You have experience creating structured apps in C#, but no experience with object-oriented programming. You need to gain experience before starting work on the company software. You decide to create a simple banking app that includes "Customer" and "Account" classes.

This exercise includes the following tasks:

1. Create a console app and a class named "Customer"

1. Add public fields and updated constructors to the "Customer" class

1. Create a class named "Account" that includes instance constructors

1. Implement static constructors for the "Account" class

## Task 1: Create a console app and a class named "Customer"

In this task, you create a new console app, add a `Customer` class to the project, and then create a class definition for the `Customer` class. The class definition includes public fields and a parameterless constructor.

Use the following steps to complete this task:

1. Open Visual Studio Code.

1. Use Visual Studio Code to open a new folder named **My CSharp Projects** that's located in the Windows Desktop folder.

    For example:

    1. On the Visual Studio Code welcome screen, select **Open Folder**. If the Welcome page isn't displayed in the editor, open the **File** menu and select **Open Folder**.
    1. In the **Open Folder** dialog box, navigate to the Windows Desktop folder.
    1. Select **New Folder** and name the folder **My CSharp Projects**.
    1. Select the **My CSharp Projects** folder and then select **Select Folder**.

1. Use the Command Palette to create a new console app named **Classes_M1**.

    1. To open the Command Palette, press **Ctrl+Shift+P**.
    1. In the Command Palette, type **.NET:** and then select **.NET: New Project**.
    1. In the **Create a new .NET Project** box, select **Console App**.
    1. In the **Name the new project** box, type **Classes_M1** and then press Enter.
    1. In the **Select location for the project** box, select **Default directory**
    1. In the **Create project or view options** box, select **Create project**

    You should see a new console app project named **Classes_M1** in the Visual Studio Code EXPLORER view.

1. If the Welcome page is still open in the Visual Studio Code editor, close the Welcome page.

1. In the EXPLORER view, collapse the **MY CSHARP PROJECTS** folder structure, and then select **SOLUTION EXPLORER**.

    The Solution Explorer in Visual Studio Code is a feature provided by the C# Dev Kit extension. It offers a structured view of your application, its solutions, and its projects, making it easier to manage .NET projects within VS Code. When you open a workspace containing .NET solution files or project files, the Solution Explorer will automatically appear and load the solution files.

    Key features of the Solution Explorer include:

    - Automatically loading single or multiple solution files in a workspace.
    - Remembering the last loaded solution file for a workspace.
    - Providing context menu options for managing solutions and projects.
    - Supporting Solution Folders for organizing projects within a solution.

1. Under **SOLUTION EXPLORER**, expand the **Classes_M1** solution and locate the **Program.cs** file.

    The structure of your solution should be similar to the following example:

    ```plaintext
    Classes_M1
        Classes_M1
            Dependencies
            Program.cs
    ```

1. Hover the mouse pointer over the two **Classes_M1** "folders" to reveal its association to the solution.

    The **Classes_M1** folder at the top level of the solution represents the solution folder. The **Classes_M1** folder nested under the solution folder represents the project folder. The **Program.cs** file is located within the project folder.

1. Open the **Program.cs** file, and then delete the existing "hello, world" code.

1. Right-click the **Classes_M1** project, and then select **New File**.

1. In the **Create a new file** dropdown, to create a class file named Customer.cs, select **Class** and then enter **Customer**.

    You should see a new file named **Customer.cs** in the Visual Studio Code editor. The file should be located in the **Classes_M1** project folder, and the code should look similar to the following code snippet:

    ```csharp

    using System;

    namespace Classes_M1;

    class Customer
    {
    
    }

    ```

    At this point, your `Customer` class definition is empty. You'll add constructors and fields to the class during this task.

1. Notice that a `Classes_M1` namespace is specified.

    A namespace is a way to organize code in C#. It provides a way to group related classes and other types into a single unit. You can use this namespace to access the `Customer` class from other classes in the project.

1. To create a constructor for the `Customer` class, add the following code to your `Customer` class definition:

    ```csharp

    public Customer()
    {
        Console.WriteLine("Customer created");
    }

    ```

    The `Customer` class now includes a parameterless constructor that writes a message to the console when a new instance of the `Customer` class is created.

1. Your updated `Customer` class should now look like the following code snippet:

    ```csharp

    public class Customer
    {
        public Customer()
        {
            Console.WriteLine("Customer created");
        }
    }

    ```

1. To create a second constructor that accepts parameters for the customer's first and last name, add the following code to your `Customer` class definition:

    ```csharp

    public Customer(string firstName, string lastName)
    {
        Console.WriteLine($"Customer created with name: {firstName} {lastName}");
    }

    ```

    The `Customer` class now includes a second constructor that accepts parameters for the customer's first and last name. The constructor writes a message to the console that includes the customer's first and last name when a new instance of the `Customer` class is created.

1. Your updated `Customer` class should now look like the following code snippet:

    ```csharp

    public class Customer
    {
        public Customer()
        {
            Console.WriteLine("Customer created");
        }

        public Customer(string firstName, string lastName)
        {
            Console.WriteLine($"Customer created with name: {firstName} {lastName}");
        }
    }

    ```

1. Switch to the Program.cs file

    The Program.cs file is where you write the code that creates instances of the `Customer` class.

1. In the Program.cs file, add the following code to create an instance of the `Customer` class:

    At this point, the Program.cs file should be empty. If the "hello, world" code is still present, delete it now.

1. Add a `using` statement that specifies the namespace defined by the customer `Customer` class.

    ```csharp

    using Classes_M1;

    ```

    This `using` statement allows you to access the `Customer` class from within the Program.cs file.

1. To create an instance of the `Customer` class, add the following code to the Program.cs file:

    ```csharp

    Customer customer = new Customer();

    ```

    The `new` operator is used to create a new instance of the `Customer` class. The `Customer` class constructor is called when the new instance is created.

1. To create a second instance of the `Customer` class that uses the new constructor, add the following code to the Program.cs file:

    ```csharp

    Customer customer2 = new Customer("John", "Doe");

    ```

    The `Customer` class constructor that accepts parameters for the customer's first and last name is called when the new instance is created. The constructor writes a message to the console that includes the customer's first and last name.

1. Take a minute to review your code.

    Program.cs file:

    ```csharp

    using Classes_M1;
    
    Customer customer1 = new Customer();

    Customer customer2 = new Customer("John", "Doe");
    
    ```

    Customer.cs file:

    ```csharp

    using System;

    namespace Classes_M1;

    public class Customer
    {
        public Customer()
        {
            Console.WriteLine("Customer created");
        }

        public Customer(string firstName, string lastName)
        {
            Console.WriteLine($"Customer created with name: {firstName} {lastName}");
        }
    }

    ```

1. Ensure that you've saved your changes to both files.

    Visual Studio Code can be configured to automatically save changes for you. If you haven't configured Visual Studio Code to automatically save changes, you can manually save your changes by selecting **File** > **Save** or **File** > **Save ALL** from the top menu bar.

1. To ensure that your solution builds without errors, right-click the **Classes_M1** solution in the Solution Explorer, and then select **Build**.

    If you don't see the **Build** option listed, ensure that you've selected the **Classes_M1** solution in the Solution Explorer. The **Build** option isn't available when a project is selected.

    You need to fix any errors before you can run your app.

1. To run your app, right-click the **Classes_M1** project in the Solution Explorer, select **Debug**, and then select **Start New Instance**.

    If you don't see the **Debug** option listed, ensure that you've selected the **Classes_M1** project in the Solution Explorer. The **Debug** option isn't available when a solution is selected.

    There are several ways to run your app in Visual Studio Code. For example:

    - You can use the **Run** menu
    - You can select the **Run** button in the top menu bar
    - You can use the **F5** key
    - You can use the Terminal panel and type `dotnet run`

    Any of these options is fine. Some options are more convenient than others, depending on your preferences. Also, some options use the debugger, which can be helpful when you need to step through your code.

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    Customer created
    Customer created with name: John Doe

    ```

## Task 2: Add public fields and updated constructors to the "Customer" class

In this task, you add public fields to the `Customer` class, update the instance constructors to use additional parameters, and then update the Program.cs file to access each object's public data.

Use the following steps to complete this task:

1. Open the Customer.cs file.

1. Add public fields to the class definition for `fName`, `lName`, and `accNumber`. Initialize the fields using default values.

    ```csharp

    public string fName = "unknown";
    public string lName = "unknown";
    public int accNumber = 0;

    ```

1. Update the second constructor to assign constructor parameters to the local variables.

    ```csharp

    public Customer(string firstName, string lastName)
    {
        fName = firstName;
        lName = lastName;

    ```

1. Update the `Console.WriteLine()` messages in both constructors to use the values stored in data fields.

    ```csharp

    public Customer()
    {
        Console.WriteLine($"Customer created: {fName} {lName}");
    }

    public Customer(string firstName, string lastName)
    {
        fName = firstName;
        lName = lastName;

        Console.WriteLine($"Customer created: {fName} {lName}");
    }

    ```

1. Switch to the Program.cs file

1. Create local variables for `firstName`, `lastName`, and `accountNumber`. .

    ```csharp

    string firstName = "John";
    string lastName = "Doe";
    string accountNumber = "12345";

    ```

1. Update the code that creates the second instance of the `Customer` class to use local variables.

    ```csharp

    firstName = "Jane";
    Customer customer2 = new Customer(firstName, lastName);
    ```

1. Add code that 
1. Review the code.

    Program.cs file:

    ```csharp

    using Classes_M1;

    namespace Classes_M1;

    string firstName = "John";
    string lastName = "Doe";
    string accountNumber = "12345";

    Customer customer = new Customer();

    string firstName = "Jane";
    Customer customer2 = new Customer(firstName, lastName);

    ```

    Customer.cs file:

    ```csharp

    using System;

    namespace Classes_M1
    {
        public class Customer
        {
            public string fName = "unknown";
            public string lName = "unknown";
            public int accNumber = 0;

            public Customer()
            {
                Console.WriteLine($"Customer created: {fName} {lName}");
            }

            public Customer(string firstName, string lastName)
            {
                fName = firstName;
                lName = lastName;

                Console.WriteLine($"Customer created: {fName} {lName}");
            }
        }
    }

    ```

1. Run your updated app and verify that you get the following output:

    ```plaintext

    Customer created: unknown unknown
    Customer created: Jane Doe

    ```

1. In the Customer.cs file, create a new instance constructor that accepts parameters for the first name, last name, and account number.

    ```csharp

    public Customer(string firstName, string lastName, int accountNumber)
    {
        fName = firstName;
        lName = lastName;
        accNumber = accountNumber;

        Console.WriteLine($"Customer created. Name: {fName} {lName}, Account: {accNumber}");
    }

    ```

1. Update the `Console.WriteLine()` messages in the first two constructors to match the message in the third constructor.

1. In the Program.cs file, create a third instance of the Customer class that uses the new constructor.

    ```csharp



    ```

1. Take a minute to review your code.

    Program.cs file:

    ```csharp

    
    ```

    Customer.cs file:

    ```csharp



    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Task 3: Create a class named "Account" that includes instance constructors

In this task, you create an `Account` class that includes instance constructors that accept parameters for the account number, account type, and balance.

Use the following steps to complete this task:

1. Use the Command Palette to create a class named `Account`.

1. next step

1. next step

1. next step

1. Take a minute to review your code.

    Program.cs file:

    ```csharp

    using System;
    using Classes_M1;

    namespace Classes_M1
    {
        class Program
        {
            static void Main(string[] args)
            {
                Customer customer = new Customer();
                string firstName = "Jane";
                Customer customer2 = new Customer(firstName, "Doe");
                Customer customer3 = new Customer("John", "Smith");

            }
        }
    }
    
    ```


    ```csharp


    
    ```

1. Run the app

1. Review the output in the terminal window.

    You should see the following output:

    ```plaintext

    ```

## Task 4: Implement static constructors for the "Account" class

In this task, you create a static constructor for the `Account` class that initializes a static field.

Use the following steps to complete this task:

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
