# Build Web Application with Blazor

# Create and run a Blazor web app
- Check the .NET 6.0 SDK, the app uses the .NET 6.0 SDK

```
dotnet --list-sdks
```

- Create the new Blazor web app

```
dotnet new blazorserver -f net6.0
```

- Run the application
```
dotnet watch run
```

# Razor components

# What is a Razor?
Razor is a markup syntax that uses HTML and C# for writing UI components of Blazor web apps.

Razor is based on ASP.NET and designed for creating web apps.

# What are Razor components?
A Razor file defines components that make up a portion of the app UI. Components in Blazor are analogous to user controls in ASP.NET Web Forms.

If you explore the project, you'll see that most files are .razor files.

At compile time, each Razor component is built into a .NET class. The class includes common UI elements like state, rendering logic, lifecycle methods, and event handlers.

# Data binding and events
# Data binding techniques are:
- C# code-behind in seperate files: 
In Blazor, you can add C# files directly to your app project, as with other .NET projects. Commonly called code-behind, this technique uses separate code files to store app logic. Separate files are a great strategy when your business logic is complex, long, or has multiple classes.

- C# inline in components:
It's a common practice to mix HTML and C# in a single Razor component file. For simple components with lighter code requirements, this approach works well. To add code into a Razor file, you'll use directives.

# What are Razor directives?
Razor directives are component markup used to add C# inline with HTML. With directives, developers can define single statements, methods, or larger code blocks.

# Code directives
Code directives should be familiar to developers who have used Razor in MVC or Pages.

You can use ```@()``` to add a C# statement inline with HTML. If you require more code, use the ```@code ```directive to add multiple statements, enclosed by parentheses.

You can also add an ```@functions``` section to the template for methods and properties. They're added to the top of the generated class, where the document can reference them.

# Page directive
The ```@Page``` directive is special markup that identifies a component as a page. You can use this directive to specify a route. The route maps to an attribute route that the Blazor engine recognizes to register and access the page.

# Razor data binding
Within Razor components, you can data bind HTML elements to C# fields, properties, and Razor expression values. Data binding allows two-way synchronization between HTML and Microsoft .NET.

Data is pushed from HTML to .NET when a component is rendered. Components render themselves after event-handler code executes, which is why property updates are reflected in the UI immediately after an event handler is triggered.

You can use ```@bind``` markup to bind a C# variable to an HTML object. You'll define the C# variable by name as a string in the HTML. You'll see an example of data binding in the following exercise.

# Create a ToDo Page
```
dotnet new razorcomponent -n Todo -o Pages
```
The ```-n|--name``` option in the preceding command specifies the name of the new Razor component. The new component is created in the project's Pages folder with the ```-o|--output ```option.

[Continue the tutorial](https://learn.microsoft.com/en-us/training/modules/build-blazor-webassembly-visual-studio-code/7-exercise-razor-binding?pivots=vscode)

# Interact with Data in Blazor web apps

# Create a user interface with Blazor components
Blazor components let you define webpages or portions of HTML that include dynamic content by using .NET code. In Blazor, you can formulate dynamic content by using C#, instead of using JavaScript.

[Learn more about Blazor components](https://learn.microsoft.com/en-us/training/modules/interact-with-data-blazor-web-apps/2-create-user-interfaces-with-blazor-components)

Here's a simple example of a Blazor component:

```
@page "/index"

<h1>Welcome to Blazing Pizza</h1>

<p>@welcomeMessage</p>

@code {
  private string welcomeMessage = "However you like your pizzas, we can deliver them blazing fast!";
}
```

In this example, the code sets the value of a string variable, named welcomeMessage. That variable is rendered within ```<p>``` tags in the HTML. We'll examine more complex examples later in this unit.

