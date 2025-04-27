# Assignment: **School Records Assignment**

## Instructions

You are building a **School Management System** using Object-Oriented Programming in C#.  
This assignment focuses on:

- **Classes and Inheritance**
- **Polymorphism** through method overriding
- **Encapsulation** by using **private data members**
- **Pass by Reference** using the `ref` keyword
- **Pass by Reference** using the `ref` keyword

---

## Requirements

1. **Create a base class** called `Person`:
   - Data Members: `id`, `name`, `dateOfBirth`
   - Constructor that sets `name` and `dateOfBirth`, and automatically assigns a unique `id`.
   - A method `DisplayInfo()` that prints the person's information.

2. **Create two classes that inherit from `Person`**:
   - `Student`
     - Data Member: `gradeLevel`
     - Private Data Member: `List<Course> enrolledCourses`
     - Methods: `EnrollInCourse(Course course)`, `ListCourses()`
     - Override `DisplayInfo()` to show the student's grade level.
   
   - `Teacher`
     - Data Member: `subjectSpecialty`
     - Private Data Member: `List<Course> coursesTeaching`
     - Methods: `AssignCourse(Course course)`, `ListCoursesTeaching()`
     - Override `DisplayInfo()` to show the teacher’s subject specialty.

3. **Create a `Course` class**:
   - Data Members: `courseName`, `courseCode`, `teacher`
   - Private Data Member: `List<Student> enrolledStudents`
   - Methods: `AssignTeacher(Teacher teacher)`, `EnrollStudent(Student student)`, `ListStudents()`

4. **Implement pass-by-reference**:
   - Create a method that updates a `Student`'s `gradeLevel` **by reference**.
   - Example method signature:
     ```csharp
     void PromoteStudent(ref Student student)
     ```

5. **Demonstrate polymorphism**:
   - Create a `List<Person>`.
   - Add both `Student` and `Teacher` objects.
   - Loop through the list and call `DisplayInfo()`.

---

## Extra (Optional)

- Add a simple console menu to allow adding students, teachers, and enrolling students into courses.

---

## Deliverables

- Full working code
- Clear demonstration of:
  - Inheritance
  - Encapsulation (private data members)
  - Polymorphism
  - Pass-by-reference

---

## Key Concepts to Remember

| Concept | Where it Appears |
|:--------|:-----------------|
| **Inheritance** | `Student` and `Teacher` inherit from `Person` |
| **Encapsulation** | Use of **private** data members |
| **Polymorphism** | `DisplayInfo()` method overridden |
| **Pass-by-reference** | `PromoteStudent(ref Student student)` method |

---

## Example Pass-by-Reference Method

```csharp
public static void PromoteStudent(ref Student student)
{
    student.gradeLevel++;
    Console.WriteLine($"{student.name} has been promoted to Grade {student.gradeLevel}.");
}
