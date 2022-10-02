# Java-basic HelloWorld

public class HelloWolrd {
    public static void main(String[] args) {
        System.out.println("HelloWolrd");

    }
}
--------------------------------------------------------------------------------
//Data type , function,wrapper classes nothing but Integer,Long,Float

public class BankAccount {
    Long     accountNumber   = 123456789l;
    String   accoundhoder    = "karthick";
    Integer  accountbalance  =  123;
    // the void keyword specifies that a method should not have a return value
    public void getBalacence(){
        System.out.println("Account Holder Name  is  "+accoundhoder);
    }
//excution the code compiler
    public static void main(String[] args) {
        BankAccount account = new BankAccount();
        account.getBalacence();
    }}
---------------------------------------------------------------------------------------
//reture Type leaning Explanation

public class CollectionAmount {
    int collectAmount= 1225;
    //A Return Statement cause the program control to transfer back the caller of a method
    public int collectAmountAndGiveItToMe(){
        System.out.println("Daddy have colleted amount "+collectAmount + " and send it to you");
        return collectAmount;//
    }
    public static void main(String[] args) {
        CollectionAmount mySon = new CollectionAmount();
        int amount = mySon.collectAmountAndGiveItToMe();
        System.out.println("Got the amount My Son " + amount);
    }}
-------------------------------------------------------------------------------------------
contractor
1,default constructors
 String student_Name;
 int    rollNo;
    /*example for default constructors.
    Do you see any constructors here? NOPE! then have no special power. Compiler has created one here!!!
    Believe me */
    public static void main(String[] args) {
        student student = new student();
        System.out.println(student.student_Name);
        System.out.println(student.rollNo);
    }}
2, No arguments constructor
public class Employee {
    //define a No arguments constructor. This is nt defult
    int     employeeId;
    String  employeeName;
    Employee(){
      employeeId = 12;
      employeeName="karthick";
        System.out.println("Employee obj is created");
    }
    public static void main(String[] args) {
       Employee employee = new Employee();
        System.out.println(employee.employeeId);
        System.out.println(employee.employeeName);
    }}
3, Parameterized Constructor
public class Animal {
    // A Parameterized Constructor. It has arguments (parameters)......
    String animal_name;String animal_type;
    Animal(String name,String type){
        animal_name = name;
        animal_type = type;
    }
    public void sayAboutAnimal(){
        System.out.println("Animal name is " +animal_name + " and Animal type is "+ animal_type);
    }
    public static void main(String[] args) {
        Animal animal1 = new Animal("duck","omnivores");//name na tiger,type omnivores na anaithunni
        Animal animal2 = new Animal("tiger","omnivores");
        Animal animal3 = new Animal("dog","omnivores");
        animal1.sayAboutAnimal();
        animal2.sayAboutAnimal();
        animal3.sayAboutAnimal();
    }}
 4,contractor overloading
 public class Draw {
    //over loading
   Draw(){
        System.out.println("Draw the object");
    }// having only parameterized constructor and calling no arg constructor. got error /* ***  */
    Draw(String toDraw){
         String draw = toDraw;
        System.out.println("drawing to "+toDraw);
    }
    public static void main(String[] args) {
        Draw draw= new Draw();
        Draw draw1= new Draw("circle");
    }}
5,Super Keyword EX ---> Work in Inheritance

public class parentClass {

    public parentClass() {
        System.out.println("Parent class");
    }}
    
    public class ChildClass extends parentClass{
    public ChildClass(){
        //Super is there without see my eye
        System.out.println("child constructor");
    }
    public static void main(String[] args) {
        ChildClass childClass = new ChildClass();
    }}
   --------------------------------------------------------------------------------------------------
   

 
    


    













































































































































































