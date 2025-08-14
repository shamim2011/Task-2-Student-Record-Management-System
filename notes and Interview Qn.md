## 💡 What it Does:
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



***4.What is constructor overloading?***  
**Ans**   
Constructor overloading in Java means defining multiple constructors in a class with different parameter lists.  
🔹 Key Points:  
Same constructor name (ClassName), but different number or types of parameters.  
Helps in initializing objects in different ways. 
class Student {  
    int id;  
    String name;  

    // Constructor 1  
    Student() {  
        id = 0;  
        name = "Unknown";  
    }  

    // Constructor 2  
    Student(int id) {  
        this.id = id;  
        name = "Unknown";  
    }  

    // Constructor 3  
    Student(int id, String name) {   
        this.id = id;  
        this.name = name;  
    }   
}  

***5.How does garbage collection work in Java?***  
**Ans**  
Garbage Collection in Java (Short Explanation):  
In Java, Garbage Collection (GC) is the process of automatically identifying and removing unused (unreachable) objects from memory (heap) to free up space and avoid memory leaks.  
Key Points:  
Java uses an automatic garbage collector, so developers don’t need to manually free memory.  
An object becomes eligible for GC when no live thread can access it (i.e., no references to it).  
GC mainly works in the heap memory.  
JVM uses algorithms like Mark and Sweep, Generational GC, and G1 GC.  
Student s = new Student(); // Object created  
s = null; // Now eligible for GC  

***6.Why do we use getters and setters?***   
**Ans**  
Getters and setters in Java are used to:  
Encapsulate data – They hide the internal representation of the object.  
Control access – You can make a field private and expose it safely through getters/setters.  
Add validation logic – Setters can include checks before assigning a value.  
Improve maintainability – Internal field names/types can change without affecting external code.  
Enable read-only or write-only access – By omitting either the getter or setter.  


private int age;  
public int getAge() {  
    return age;  
}  

public void setAge(int age) {  
    if(age > 0) {  
        this.age = age;  
    }  
}  

***7.What is a static variable?***  
**Ans**  
In Java, a static variable is a variable that belongs to the class rather than to any specific object (instance).  
✅ Key Points:  
Declared using the static keyword.  
Shared among all instances of the class.  
Memory is allocated only once, when the class is loaded.  
Accessed using the class name (e.g., ClassName.variableName).  

class Example {  
    static int count = 0; // static variable  

    Example() {  
        count++;  
    }  
}  

public class Main {  
    public static void main(String[] args) {  
        new Example();  
        new Example();  
        System.out.println(Example.count); // Output: 2  
    }  
}  


***8.What is the use of final keyword?***  
**Ans**  
In Java, the final keyword is used to restrict modification. Its meaning depends on where it's used:  
Final variable: Value cannot be changed (like a constant).  
final int x = 10;  
x = 20; // Error  

Final method: Method cannot be overridden by subclasses.  
class A {  
    final void show() {}  
}  

class B extends A {  
    void show() {} // Error  
}  

Final class: Class cannot be extended.  
final class A {}  

class B extends A {} // Error  


***9..Difference between compile-time and runtime errors?***  
**Ans**  
Difference between Compile-time and Runtime Errors in Java (Short):  

Aspect ->	Compile-time Error	-> Runtime Error  
When Occurs	-> During code compilation	-> During program execution  
Detected By	-> Compiler	-> JVM (Java Virtual Machine)  
Examples	-> Syntax errors, missing semicolon, type mismatch	-> Division by zero, null pointer exception  
Fixing	-> Must be fixed before code runs	-> May not be noticed until specific input/scenario  

Summary:  
Compile-time errors stop the program from compiling.  
Runtime errors occur while the program is running.   
***10.What are access modifiers?***  
**Ans**  
In Java, access modifiers are keywords used to set the visibility or access level of classes, methods, variables, and constructors.  

Four Main Access Modifiers:  

Modifier	Access Level  

public	-> Accessible from anywhere  
protected	-> Accessible within the same package and subclasses (even in different packages)  
(default)	-> Accessible only within the same package (no modifier)  
private	-> Accessible only within the same class  

public class Example {  
    public int a;        // accessible everywhere  
    protected int b;     // accessible in same package + subclasses  
    int c;               // default access (package-private)  
    private int d;       // accessible only inside this class  
}  
