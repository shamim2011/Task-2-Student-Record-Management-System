### 💡 What it Does:
 ⨀ Uses a Student class with private fields and getter/setter methods.  
 ⨀ Stores all records in an ArrayList<Student>.  
 ⨀ Provides a loop-driven console menu for user interaction.  
 ⨀ Simple, efficient, and beginner-friendly system for practicing OOP and collections in Java.   


### Interview Questions:

***1.What is encapsulation?***  
**Ans:**  ✅ Method Overloading in Java
Method Overloading is a feature in Java that allows a class to have more than one method with the same name, as long as their parameter lists are different (either in number, type, or order of parameters).

🔍 Key Points:
It improves code readability and reusability.

It happens at compile time → also called Compile-Time Polymorphism or Static Polymorphism.

Return type can be different, but it alone can't be used to overload a method.

✅ How Can Methods Be Overloaded?
By changing the number of arguments

By changing the data type of arguments

By changing the order of arguments (if types are different)

***2.How do you handle divide-by-zero?***  
**Ans**  1. Using if check (for integers or doubles)
if (denominator != 0) {
    int result = numerator / denominator;
} else {
    System.out.println("Cannot divide by zero.");
}
2. Using try-catch block (for integers)
try {
    int result = num1 / num2;
} catch (ArithmeticException e) {
    System.out.println("Error: Division by zero is not allowed.");
}
📝 Note: ArithmeticException is only thrown for integer division, not for double division.

3. For double values
No exception is thrown, but result is:

Infinity if divided by 0.0

NaN (Not a Number) if 0.0 / 0.0

double result = 10.0 / 0.0;   // result = Infinity


***3.Difference between == and .equals()?***  
**Ans**  
Use == for:

Comparing primitive types

Checking if two object references point to the same object  

Use .equals() for:  

Comparing values/content of two objects
String a = new String("Java");
String b = new String("Java");

System.out.println(a == b);        // false (different objects)
System.out.println(a.equals(b));   // true  (same content)

***4.What are the basic data types in Java?***  
**Ans**   
In Java, the basic (or primitive) data types are:

byte – 8-bit signed integer (range: -128 to 127)  
short – 16-bit signed integer (range: -32,768 to 32,767)  
int – 32-bit signed integer (range: -2,147,483,648 to 2,147,483,647)  
long – 64-bit signed integer (range: -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807)  
float – 32-bit floating point number (single precision)  
double – 64-bit floating point number (double precision)  
char – 16-bit Unicode character (range: '\u0000' to '\uffff')  
boolean – represents true or false values  
***5.How is Scanner used for input?***  
**Ans**  
Scanner scanner = new Scanner(System.in); creates a scanner to read input from the keyboard.  
Methods like nextInt() and nextLine() read different types of input.  
Always close the scanner with scanner.close(); when done.  
***6.Explain the role of a loop.***  
**Ans**  
🔁 Role of a Loop in Java
A loop in Java is used to execute a block of code repeatedly as long as a specified condition is true.  
It helps reduce code duplication and makes programs more efficient and dynamic.  
✅ Why Use Loops?  
To repeat tasks automatically  

To iterate over arrays, lists, or collections  

To process input/output continuously  

To perform tasks like searching, counting, etc.  
for loop -> When the number of iterations is known  
while loop	-> When the condition is checked before each run  
do-while loop	-> Executes at least once, checks condition later  
for-each loop	-> Used to traverse arrays or collections  
***7.Difference between while and for loop?***  
**Ans**  
✅ Difference Between for and while Loop (Short)
for loop is used when the number of iterations is known. All loop control (init, condition, update) is in one line.  
while loop is used when the number of iterations is unknown, and the condition is checked before each iteration.  
for is compact and best for counting; while is flexible and suits dynamic conditions.  


***8.What is the JVM?***  
**Ans**  
✅ JVM (Java Virtual Machine) – Short Definition  
The JVM (Java Virtual Machine) is a part of the Java Runtime Environment (JRE) that executes Java bytecode.  
It allows Java programs to run independently of the underlying hardware and OS (i.e., Write Once, Run Anywhere).  
🔧 Key Roles of JVM:  
Loads and verifies .class files (bytecode)  
Executes bytecode line by line  
Manages memory (Garbage Collection)  
Ensures security and portability  
***9.How is Java platform-independent?***  
**Ans**  
✅ Why Java is Platform-Independent (Short)  
Java is platform-independent because Java code is compiled into bytecode, which is not specific to any platform.  
This bytecode runs on the Java Virtual Machine (JVM), and since each platform (Windows, Linux, Mac) has its own JVM implementation, the same Java program can run anywhere the JVM is installed.  

🧠 Key Phrase:  
"Write Once, Run Anywhere" — thanks to bytecode and JVM.  
***10.How do you debug a Java program?***  
**Ans**  
✅ How to Debug a Java Program (Short)  
Use Print Statements  
Insert System.out.println() to check variable values and flow.  
Use an IDE Debugger (like IntelliJ or Eclipse)  
Set breakpoints  
Step through code (Step Into, Step Over)  
Inspect variables, call stack, and watch expressions  
Use Exception Messages  
Read stack traces to locate the exact error line.  
Use Logging  
Replace prints with logging (java.util.logging, Log4j) for better control.  
Test in Small Parts  
Break code into methods and test individually (unit testing).  
