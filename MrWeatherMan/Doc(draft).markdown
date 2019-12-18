
# Learning MVC ASP.net

### What is ASP.Net, and ASP.Net Core
ASP.Net is a framework or library of code from many different developers that make it fast and easy to develop
applications. It is basically a standard that everyone can use so they don't have to write code that has already
been written over and over again.

ASP.Net Core is an open source version of ASP.Net that is cross-platform and uses the C# or F# programming language.

### What is MVC and why do I care?
MVC stands for Model, View, Controller. It is nothing more than a way of coding. It is better to have a well-defined
structure for your code so when your code changes for example: adding a new feature, or updating to a new version
it will be far easier and save headaches and time. As a bonus if some error is in the code it can also be easier to
track down and correct it makes code easier to maintain.

###### TODO: Add image or other resource to help understand MVC

### Some things you will need before starting:

- A drive to learn and figure problems out (anyone can learn how to code!)
- A computer that can install ASP.NET Core
- An IDE is needed for the sane individual. The "perferred" editor for ASP.Net is usually Visual Studio I am using Visual Studio Community 2019, it is free
- You should know I am not an experienced ASP.Net developer, I am learning and as I learn I am publishing what I learn to hopefully help at least one other person.

### What to do if you get stuck on an issue
By the time you follow this tutorial things might be old or broken if I don't keep everything
updated. A very important part of learning how to code is learning to deal with problems and solve them.
There are great resources to help you find ways to solve any problem you might have. I personally am
learning and writing this course with help from Google and the great people that answer our questions everyday.
Other than Google, another great resource is the code docs! You don't have to read everything and remember it all.
My goal is not to learn everything about a certain programming language, it is to build applications using the
tools we already have.

You can always look back at the [Github](https://github.com/ch4nc3l0/MrWeatherMan-Weather-Learning-MVC-ASP.NET) page I will make commits in a structured way to allow anybody to look for what 
they are stuck on.

### Setting up the development Environment

###### Using VS Communtiy Edition

1. [Download](https://visualstudio.microsoft.com/vs/community/) Visual Studio and install it.
2. At the setup page select the ASP.NET and web development option. (You can select other options too if you want them installed)
3. To make sure everything was installed correctly startup VS. Select start a new project and select the ASP.Net Core option. There are many different templates the one we want is the MVC (Model View Controller) template.

###### Using ASP.Net Core Only
1. [Download](https://dotnet.microsoft.com/?&ef_id=CjwKCAiAluLvBRASEiwAAbX3GY4wsBwj3cTPrBdbboU-SXnC-cHS8lEtNvWgFMQk_Rhe05XQLZmEWRoCFgoQAvD_BwE:G:s&_aid=&OCID=AID2000725_SEM_CjwKCAiAluLvBRASEiwAAbX3GY4wsBwj3cTPrBdbboU-SXnC-cHS8lEtNvWgFMQk_Rhe05XQLZmEWRoCFgoQAvD_BwE:G:s)
ASP.Net Core and install it.
2. Type in dotnet into your console to see if everything installed correctly.
3. I will personally be moving forward with the tutorial using VS. I will not be 
providing a step by step for this environment at the moment. Everything is still
possible using only ASP.Net Core.

### C#
C# is a programming language that gives developers alot of control compared to something like javascript.
Because the developer has more control it has a little bit more of a learning curve. More control normally 
means more things to manage.

### Enough Reading! Lets Code!
We will write a guessing game application! That is right I said we! There are exercises in every lesson, you can move
forward and see the solution but I highly recommend at least trying every exercise at least once. It will teach you to
use what you just learned and force you take a break from reading and copy/paste coding.

### Your first C# Program
1. In VS click create new project
2. Select Console App (.netcore)
3. Give it a name I used LearningCSTut
4. Click Create

VS generated some code for us! We can press run in VS and run the code.
A terminal window should have popped up and have the words Hello World!

Congragulataions! That is the starter template for a program in C#. Lets look
closer at the code and understand what is going on.

```
using System;

namespace LearningCSTut
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("Hello World!");
        }
    }
}
```

---
```
using System;
```

using - here is a keyword in C# that tells the compiler we are going to use something 
from another file.

System - a namespace you can think of it as a filename, we have to tell c# what the
file is called before we use it. We didn't write anything called System but it is already
in the .Net Framework
 
---
```
namespace LearningCSTut {
```

namespace - Now we are declaring our own custom namespace or "file" it 
is not really a file and can be different than the actual file name,
and you can have nested namespaces or a namespace in a namespace.
Think of it as a "file name" for a section of code.

LearningCSTUT - This is just a name for the namespace we can name it
whatever we want to. It is best practice to name it based on what you
are doing with it.

{ - This is an opening bracket we put all the code we want the 
namespace to have inside of the brackets.

---
```
class Program
{
```

class - A way to combine multiple fields of code into one unit typically
classes hold functions and data (we will look at functions in the next line)

Program - The user-defined name for the class we will use this name to call
the class when we want to use it later. 

---
```
static void Main(string[] args)
{
```

static - Declares that this funtion or method should only have one instance
that is identical whenever it is used. It is not for a class or variable with
many instances with different values.

void - This is called a return type, we are saying that this function or method 
is not returning any value.

Main - This is a special function or method that is called when the app starts.
a function or method is a group of code that performs a certain function. Normally
you want functions to be a group of code that performs one task.

(string[] args) - This is called parameters we are telling the program that the 
main function takes in a string or group of letters called args. The []next to string
means string is an array, we will go over arrays at a later time.

{ - Another opening bracket exept now the code in this bracket is the code 
we want inside of the main method.

---
```
Console.WriteLine("Hello World!");
```

Console - A class from the System namespace 

.WriteLine - A method from the Console class this method outputs text to the screen
this method and class are provided to us by the ASP.Net framework.

("Hello World!"); - This is the parameter for the WriteLine method, it tells WriteLine
to print the string Hello World! to the console. The semicolon here means we are done
telling c# what we want to do with the line Console.WriteLine("Hello World!"); If it was
not there C# would think the next line of code was also part of Console.WriteLine.

---
```
        }
    }
}
```

1st } - Here the closing brackets let c# know the main method is done.

2nd } - Lets c# know the method main is done.

3rd } - Lets c# know the class program is done.

---

###### First App Quiz

---

1. What are { \} used for in C#?
a. Ending one line of code.
b. Defining the start and end of a namespace, class, or method.
c. For making funny faces when your bored.
d. Used in methods to define the start and end of parameters.

---

2. Why do we have to use ; in C#?
a. To tell C# when we are done writing a line of code.
b. It makes our code look cooler.
c. Because.
d. To start a new class.

---

3. What is a function or a method?
a. A single line of code.
b. A way to run your application without errors.
c. The correct way to write a class while also using the correct namespace.
d. A section of code that normally performs one task.

---

4. What is a namespace?
a. Space in the RAM allocated to remember the name of your application.
b. A user-defined name that nobody else in the world can use.
c. They are what C# uses to track the "file name" of our block of code.
d. A variable that couldn't be saved because the hard drive was full.

---

5. What is a class in C#?
a. A place to learn C#.
b. A Method.
c. A container that can hold methods and data.
d. A way to set memory aside for slow database querys

---
6. What will this block of code do?

```
using System;

namespace LearningCSTut
{
    class Program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("This is my first program!");
        }
    }
}
```

a. Nothing that is bad code.
b. It will print to the console This is my first program!
c. It create a variable and then runs main and after that it makes a class.
d. It prints out Console.WriteLine("This is my first program!"); to the terminal window.

---

7. What does the line: `using System;` mean?
a. You are currently using your computer so you have to use the system.
b. You are using a namespace called system.
c. A method named system exists in your file.
d. The class system is on line 6 of your code.

---

8. What does the method WriteLine do?
a. It writes something onto the console based on your parameters.
b. It writes a line of code for you based on your parameters.
c. It doesn't write anything.
d. It takes the square root of your input.

---

ans 1-b 2-a 3-d 4-c 5-c 6-b 7-b 8-a