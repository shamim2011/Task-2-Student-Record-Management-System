### 💡 What it Does:
 ⨀ Uses a Student class with private fields and getter/setter methods.  
 ⨀ Stores all records in an ArrayList<Student>.  
 ⨀ Provides a loop-driven console menu for user interaction.  
 ⨀ Simple, efficient, and beginner-friendly system for practicing OOP and collections in Java.   


### Interview Questions:

***1.What is encapsulation?***  
**Ans:**  Encapsulation in Java is the concept of wrapping data (variables) and code (methods) together as a single unit, typically inside a class, and restricting direct access to some of the object's components.  
Key Points:  
Achieved using private variables and public getters/setters.  
Ensures data hiding and security.  
Helps in maintaining control over the data.  
✅ In short: Encapsulation = data hiding + access control via methods.  

***2..How are ArrayLists different from arrays?***  
**Ans**  Feature ->	Array	-> ArrayList  
Size	-> Fixed (set at creation)	-> Dynamic (resizable)  
Type	-> Can hold primitives & objects	-> Can hold only objects  
Syntax	-> int[] arr = new int[5];	-> ArrayList<Integer> list = new ArrayList<>();  
Performance	-> Faster for fixed-size data	-> Slower due to dynamic resizing  
Methods	-> No built-in methods for insert/delete	-> Many methods like add(), remove(), etc.  
Import Needed	-> No	-> Yes (java.util.ArrayList)  


***3.How to sort an ArrayList?***  
**Ans**  
✅ Example: Sorting in ascending order  
import java.util.*;

public class SortExample {  
    public static void main(String[] args) {  
        ArrayList<Integer> list = new ArrayList<>(Arrays.asList(5, 2, 8, 1, 3));  
        Collections.sort(list);  
        System.out.println(list); // Output: [1, 2, 3, 5, 8]  
    }  
}  
✅ Descending order:  
Collections.sort(list, Collections.reverseOrder());  
✅ For custom objects:  
Use a Comparator:  
Collections.sort(list, (a, b) -> a.getName().compareTo(b.getName()));  



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
