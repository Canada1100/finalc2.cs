# finalc2.cs
# Final-Assignment-Submission
using System;
using System.Linq;

namespace CodeFirstStudentApp
{
class Program
{
static void Main(string[] args)
{

using (var context = new StudentContext())
{
/
var student = new Student
{
Name = "Ashutosh",
Age = 25
};
{
            
            context.Students.Add(student);

            
            context.SaveChanges();

            
            Console.WriteLine("Student added: {0}, Age {1}", student.Name, student.Age);

            
            var students = context.Students.ToList();
            foreach (var s in students)
            {
                Console.WriteLine("Student: {0} (ID: {1})", s.Name, s.Id);
            }
        }

        Console.WriteLine("Press any key to exit.");
        Console.ReadKey();
    }
using System;

namespace CodeFirstStudentApp
{

public class Student
{
public int Id { get; set; } 
public string Name { get; set; } 
public int Age { get; set; } 
}

using System.Data.Entity;

namespace CodeFirstStudentApp
{

public class StudentContext : DbContext
{
public StudentContext() : base("StudentDB") { }

swift
Copy
Edit
    public DbSet<Student> Students { get; set; }
}
