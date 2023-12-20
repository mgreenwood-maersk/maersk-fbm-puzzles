# Pre-screening questions

## Q1: Can you tell us what TDD means to you?

TDD stands for Test-Driven Development. 

It is a software development approach in which tests are written before the code that needs to be implemented. The process typically follows these steps:

1. **Write a Test:** Before writing any code, developers create a test that defines a new function or improvement of a function, which should fail initially since the code isn't implemented yet.

2. **Write Code:** Developers then write the minimum amount of code necessary to pass the test. This often means writing just enough code to satisfy the test, but no more.

3. **Run Tests:** Run all the tests to ensure that the new code didn't break existing functionality. If any test fails, developers modify the code to make it pass.

4. **Refactor Code:** Once the tests pass, developers may refactor the code to improve its structure, readability, or efficiency, while ensuring that the tests still pass.

5. **Repeat:** The process is repeated for each new piece of functionality.

The main advantages of TDD include:

- **Early Detection of Bugs:** Since tests are written first, any issues are identified early in the development process.

- **Improved Code Quality:** TDD encourages modular and loosely coupled code, making it easier to maintain and extend.

- **Increased Confidence in Changes:** Developers can make changes to the code with confidence, knowing that existing functionality is still working as intended if the tests pass.

TDD is commonly associated with agile and iterative development methodologies, and it has become a widely adopted practice in the software development industry.
 
## Q2: What are access modifiers in C# and briefly describe how they differ?

In C#, access modifiers are keywords that define the visibility or accessibility of types and type members (such as fields, methods, properties, and events) in a program. There are four primary access modifiers in C#:

1. **public:**
   - Members with the `public` access modifier are accessible from any other code in the same assembly or another assembly that references it.
   - This is the most permissive access level.

```csharp
public class MyClass
{
    public int MyPublicField;
    public void MyPublicMethod() { }
}
```

2. **private:**
   - Members with the `private` access modifier are only accessible within the body of the containing type.
   - This is the most restrictive access level.

```csharp
public class MyClass
{
    private int myPrivateField;
    private void MyPrivateMethod() { }
}
```

3. **protected:**
   - Members with the `protected` access modifier are accessible within the containing type and by derived types.
   - This access level is commonly used in inheritance scenarios.

```csharp
public class MyBaseClass
{
    protected int MyProtectedField;
    protected void MyProtectedMethod() { }
}

public class MyDerivedClass : MyBaseClass
{
    // Can access MyProtectedField and MyProtectedMethod here
}
```

4. **internal:**
   - Members with the `internal` access modifier are accessible within the same assembly but not from outside the assembly.
   - This is useful for creating components that are only intended to be used within a specific assembly.

```csharp
internal class MyInternalClass
{
    internal int MyInternalField;
    internal void MyInternalMethod() { }
}
```

Additionally, there is an `internal protected` access modifier, which combines the behaviors of `internal` and `protected`. It allows access within the same assembly and by derived types.

```csharp
internal class MyBaseClass
{
    protected internal int MyProtectedInternalField;
    protected internal void MyProtectedInternalMethod() { }
}

public class MyDerivedClass : MyBaseClass
{
    // Can access MyProtectedInternalField and MyProtectedInternalMethod here
}
```

These access modifiers help control the visibility and interaction of different parts of your code, providing encapsulation and allowing you to enforce design principles such as information hiding and modularity.

# Q3: What is the difference between abstract classes and interfaces and when would you use one over the other?

Abstract classes and interfaces are both mechanisms in C# that allow you to define a contract for classes to implement. However, they have some key differences in their usage and characteristics.

### Abstract Classes:

1. **Abstract classes can have implementation:**
   - Abstract classes can have both abstract (without implementation) and non-abstract (with implementation) methods.
   - They can also have fields, properties, and constructors.

2. **Single Inheritance:**
   - A class can inherit from only one abstract class at a time.

3. **Access Modifiers:**
   - Abstract classes can have access modifiers for their members, allowing you to control the visibility of methods and fields.

4. **Constructors:**
   - Abstract classes can have constructors, and when a derived class is instantiated, the base class constructor is called.

5. **Usage:**
   - Use abstract classes when you want to provide a common base implementation for a group of related classes.
   - Use abstract classes when you need to declare fields or provide a common base implementation for methods.

```csharp
public abstract class Shape
{
    public abstract void Draw();

    public void Move()
    {
        Console.WriteLine("Moving the shape.");
    }
}
```

### Interfaces:

1. **No Implementation:**
   - Interfaces can only declare method signatures, properties, events, and indexers. They cannot contain any implementation.

2. **Multiple Inheritance:**
   - A class can implement multiple interfaces, allowing for a form of multiple inheritance.

3. **No Constructors:**
   - Interfaces cannot have constructors.

4. **Implicitly Public:**
   - Members of an interface are implicitly public and cannot have access modifiers.

5. **Usage:**
   - Use interfaces when you want to define a contract without providing any implementation.
   - Use interfaces when you need to support multiple inheritance or when you want to impose a certain structure on unrelated classes.

```csharp
public interface IDrawable
{
    void Draw();
}

public class Circle : IDrawable
{
    public void Draw()
    {
        Console.WriteLine("Drawing a circle.");
    }
}
```

### When to Use One Over the Other:

1. **Commonality and Reusability:**
   - If you have a group of related classes that share common behavior or state, an abstract class might be more appropriate.
   - If you have unrelated classes that need to conform to a specific contract, use interfaces.

2. **Multiple Inheritance:**
   - If you need to support multiple inheritance, interfaces are the way to go, as a class can implement multiple interfaces but can inherit from only one abstract class.

3. **Implementation Details:**
   - If you need to provide a common base implementation along with a contract, use an abstract class.
   - If you want to define a contract without providing any implementation details, use an interface.

In many cases, the choice between abstract classes and interfaces depends on the specific requirements of your design and the relationships between the classes in your system. It's not uncommon to use a combination of both in a well-designed object-oriented system.
