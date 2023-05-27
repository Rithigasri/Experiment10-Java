# EXPERIMENT 10: IMPLEMENTATION OF INHERITANCE USING CLASSES

## AIM:
To create a class named 'Member' having the following members:  
Data members:
1. Name
2. Age
3. Phone number
4. Address
5. Salary

It also has a method named 'printSalary' which prints the salary of the members. Two classes 'Employee' and 'Manager' inherits the 'Member' class. The 'Employee' and 'Manager' classes have data members 'specialization' and 'department' respectively. Now, assign name, age, phone number, address and salary to an employee and a manager by making an object of both of these classes and print the same.

## PROCEDURE:
1. Create a class named member that has elements name,age,phno,address,salary.
2. Create a class named manager that has element department.
3. Create a class named employee that has element specialisation.
4. Inherit member class for class manager and class employee.
5. Get the input from user for employee and manager.
6. Display the details.
7. End the program.

## PROGRAM:
Main.java
```
import java.util.Scanner;
public class Main {
    public static void main(String[] args)
    {
        Scanner scan=new Scanner(System.in);
        Employee emp=new Employee();
        System.out.println("Enter employee details");
        emp.name= scan.next();
        emp.age= scan.nextInt();
        emp.phno= scan.nextLong();
        emp.address= scan.next();
        emp.specialisation= scan.next();
        emp.salary=scan.nextInt();

        Manager man=new Manager();
        System.out.println("Enter manager details");
        man.name= scan.next();
        man.age= scan.nextInt();
        man.phno= scan.nextLong();
        man.address= scan.next();
        man.department= scan.next();
        man.salary=scan.nextInt();

        System.out.println("The Employee Details are: \nName: "+emp.name+"\nAge: "+emp.age+"\nPhone number: "+emp.phno+"\nAddress:
        "+emp.address+"\nSpecialisation: "+emp.specialisation);
        emp.printSalary(emp.salary);
        System.out.println("The Manager Details are: \nName: "+man.name+"\nAge: "+man.age+"\nPhone number: "+man.phno+"\n
        Address: "+man.address+"\nDepartment:"+man.department);
        man.printSalary(man.salary);
    }
}
```
Manager.java
```
public class Manager extends Member {
    String department;
}
```
Employee.java
```
public class Employee extends Member {
    String specialisation;
}
```
Member.java
```
public class Member {
    String name;
    int age;
    long phno;
    String address;
    int salary;
    public void printSalary(int sal)
    {
        System.out.println("Salary: "+sal);
    }
}
```

## OUTPUT:
![image](https://github.com/Rithigasri/Experiment10-Java/assets/93427256/b4d847da-a56b-47a1-a670-29ff3f0a9071)

## RESULT:
Hence, implementation of inheritance was done successfully.
