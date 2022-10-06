# Java-basic HelloWorld

public class HelloWolrd {
    public static void main(String[] args) {
        System.out.println("HelloWolrd");

    }
}
--------------------------------------------------------------------------------
//Data type , function,wrapper classes nothing but Integer,Long,Float,

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
conditional statement
1,If Condition
*The statement gets excuted only when the given condition is true.If the condition is false then the statement inside if 
statements body are completely ignored.
-------------------------------------------------------------------------------------------------------
2,If else condition
public  class LetsHaveACoffe {
    //boolean is data type YES OR NO
    boolean isCupEmpty = false;//change the vale is false print else statement

    public static void main(String[] args) {
        LetsHaveACoffe coffe = new LetsHaveACoffe();
        if(coffe.isCupEmpty){
            System.out.println("Fill the cup");
        }
        else{
            System.out.println("Drink the coffee");
        }
    }}
----------------------------------------------------------------------------------------------------------------
3,If else-if-if
public class WhoIsTheHero {
    String myHeroName = "Super man";//Super Man print--> Sorry i can't guess we will use
    public void superHeroGuesser(){
        if(myHeroName.equals("iron man")){
            System.out.println("Your thought about Iron man");
        }else if(myHeroName.equals("Super man")){//equalsIgnorcase/ Super MAN the will print super man
            System.out.println("Your thought about Super man");
        } else if (myHeroName.equals("Thor")){
            System.out.println("Your thought about Thor");
        }else {
            System.out.println("Sorry i can't guess");
        }
    }
    public static void main(String[] args) {
        WhoIsTheHero hero = new WhoIsTheHero();
        hero.superHeroGuesser();
    }}
    -------------------------------------------------------------------------------------------
 4,Switch case
 
 public class SuperHeroOrNot {
    //Switch case we will use the multiple condition
    String hero = "Iron man";
    public void heroOrNot(){
        switch (hero){
            case "Iron man":
                System.out.println("Iron man is a super hero");
                break;
            case "bat man":
                System.out.println("bat man is a super hero");
                break;
            case "super man":
                System.out.println("super man is a super hero");
                break;
            default:
                System.out.println(hero + "Sorry I don't know this person");
        }
    }
    public static void main(String[] args) {
        SuperHeroOrNot hero = new SuperHeroOrNot();
        hero.heroOrNot();
    }}
---------------------------------------------------------------------------------------------------------- 
Looping Statements

*When we have to perform certain operations respetedly.
1,For loop
2,While loop
3,Do while
*Loops are used to repeat a block of code.

public class Imposition {
    /* You: I'm not Sure! May be this programing is not for Me!
    *  You Traniner: what you saying ?You are doing great!
    * YOu: No!! I don't Belive! Ok.write an Imposition.
    * "I can program ! I can learn" - 25 times"*/

    public static void main(String[] args) {
        //for loop initialization; Condition; increment/decrement
       /* for(int times=0;times<25;times++){
            System.out.println("I can program ! I can learn");
        }*/
        //while loop like as for same concept
     /*   int times=0;

        while (times<25){
            System.out.println("I can program ! I can learn");
            times++;
        }*/
        int times = 0;
        do{
        System.out.println("I can program ! I can learn");
            times++;
        }while (times<25);
       }
   }
//while and do while differentiation? while loops is entry control loops and do while loops  exit control loop.
-------------------------------------------------------------------------------------------------------------------------
Static Keyword Concept
1,StaticMethods
public class StaticMethods {
    // Create a static method and call it without object.
    public static void method1(){
        System.out.println("Static method");
    }
    //we can call Static method from non static method but not otherwise.
    public  void nonStatic(){
        System.out.println("Non Static method");//StaticMethods name = new StaticMethods();name.method2();call this
    }
    public static void main(String[] args) {
        method1();
--------------------------------------------------------------------------------------------------------------------------------
2,Static Block
public class StaticBlock {
    // when u create the static {} first static will execution in order.order by order execution.
    static {
        System.out.println("Inside static block1");
    }
    //priority first static and main method it's logic......
    static {
        System.out.println("Inside static block2");
    }
    public static void main(String[] args) {
            System.out.println("Inside main method");
        }}
    --------------------------------------------------------------------------------------------------------------------------------
3,StaticVariable
public class StaticVariable {
    //Example to show,Static variable are share among objects.
    static int accountBalance = 0;
    String depositeBy;

    public static void main(String[] args) {
        StaticVariable object1 = new StaticVariable();
        object1.accountBalance=1000;
        object1.depositeBy="karthick";
        StaticVariable object2 = new StaticVariable();
        object2.accountBalance=3000;
        object2.depositeBy="kumaravel";
        StaticVariable object3 = new StaticVariable();
        object3.accountBalance=4000;
        object3.depositeBy="Mani";
        System.out.println("object integer " +object1.accountBalance);
        System.out.println("object integer " +object1.depositeBy);
        System.out.println("object integer " +object2.accountBalance);
        System.out.println("object integer " +object2.depositeBy);
        System.out.println("object integer " +object3.accountBalance);
        System.out.println("object integer " +object3.depositeBy);
    }}
--------------------------------------------------------------------------------------------------------------------------------
Inheritance (Access Modifier) Meaning reusability of code use parent and child.

public class Car {
    //Process of acquiring the properties(data +methods) we can use multiple class and data and method

    public int wheels=4;//default int wheels, Private int wheels,
    public void engine(){
        System.out.println("This my engine secret");
    }
    public static void main(String[] args) {
        Car car = new Car();
        car.engine();
    }
}
public class BMW extends Car{
    public static void main(String[] args) {
        BMW bmw = new BMW();
        bmw.engine();
    }
}
--------------------------------------------------------------------------------------------------------------
Access Modifiers:
* default - When No acess modifier is specified. EX code :int wheels
* Private - only within the class in which they are declared. EX code:private int wheels
* Protected - with same package/sub Class in difference package.EX code:protected int wheels
* Public - from everywhere in the program. EX code:Public int wheels
 */
 
Access modifiers-Same class-Same package-Sub/class-Other class
Public            -    Y     -     Y      -    Y    -     Y
protected         -    Y     -     Y      -    Y    -     N
no access modifer -    Y     -     Y      -    N    -     N
private           -    Y     -     N      -    N    -     N
--------------------------------------------------------------------------------------------------------------
Polymorphism(Is the capability of a method(fun) to do different thing based on the object that it is acting upon.) 
Type of Polymorphism Two 
1,Static /compile /early binding / (Overloading) (Method name should be same!!!)

public class TheWayWeTake {
    // we can create Parent class,Partner class,Boss class.
    // *This class is to illustration method overloading with a practical example.
    // it's called as method overloading. method name should be same. Must imp
    public void take(Parents styleOfTaking){
        System.out.println("Polite , Respectable ??");
    }
    public void take(Partner styleOfTaking){
        System.out.println("love, Romantic, Mixture of everything!!");
    }
    public  void take(Boss StyleOfTaking){
        System.out.println("Nothing personal");
    }
    public static void main(String[] args) {
        TheWayWeTake take = new TheWayWeTake();
        Parents parents = new Parents();
        take.take(parents);
        Partner partner = new Partner();
        take.take(partner);
        Boss boss = new Boss();
        take.take(boss);
}
}

Just create a class That why is upper code is working
public class Partner {
    // *This class is to illustration method overloading with a practical example
}
public class Parents {
    /*This class is to illustration method overloading with a practical example.Also it acts as the demostrate
    Overriding */
public class Boss {
    // *This class is to illustration method overloading with a practical example
}    
--------------------------------------------------------------------------------------------------------------
2,Dynamic /Runtime /late binding (@Override)

public class Parents {
    /*This class is to illustration method overloading with a practical example.Also it acts as the demostrate
    Overriding */
    public void properties(){
        System.out.println("Son!! use my property");
    }
    public void marriage(){
        System.out.println("Son !! Marry your Uncle's doughter");
    }
}
public class Son extends Parents{
    //This Class is to illustrate method overriding with a practical Example...
    // When child class not satisfying with the implementation of parent class @Override come in child class.
@Override
public void marriage(){
    System.out.println("My Marriage MY Rule....");
}
    public static void main(String[] args) {
        Parents parents = new Son();// syntax: parentClass ref = new childClass
        parents.properties();
        parents.marriage();

    }
}
--------------------------------------------------------------------------------------------------------------
Abtraction (Hiding the implementation detail)

public abstract class Car{

    public abstract void engineSecret();
    public abstract void companyVault();

    public void employee(){
        System.out.println("Employee");
    }
}
public class Bmw extends Car{
    @Override
    public void engineSecret(){
        System.out.println("BMW Engine Secret");
    }
    @Override
    public void companyVault(){
        System.out.println("BMW company vault");
    }
    public static void main(String[] args) {
        Car car = new Bmw();
        car.engineSecret();
        car.companyVault();
    }
}
public class Benz extends Car{
    @Override
    public void engineSecret() {
        System.out.println("Benz Engine Secret");
    }
    @Override
    public void companyVault() {
        System.out.println("Benz Company Vault ");}
    public static void main(String[] args) {
        Car car = new Benz();
        car.engineSecret();
        car.companyVault();

    }
}
--------------------------------------------------------------------------------------------------------------------
Interface (Like class but is not a class)

public interface EmloyeeRule {

    int salary = 25000;//By default, these variables are final and abstract
    int leaves =10;

    public void maintainHour();//By default , they are abstract
    public void relocate();
    public void report();
    public void dress();
}

public interface FamilyRules {
    public void takeCareParents();
    public void helpMembers();
    public void eatTogether();
    public void enjoy();
}
public class ABCEmployeeRule implements EmloyeeRule,FamilyRules{
    public void maintainHour(){
        System.out.println("One day working Hr 8hr");
    }
    public void relocate(){
        System.out.println("chennai");
    }
    public void report(){
        System.out.println("manager");
    }
    public void dress(){
        System.out.println("formal");
    }
    public void takeCareParents(){
        System.out.println("I love my parents");
    }
    public void helpMembers(){
        System.out.println("I help my mom");
    }
    public void eatTogether(){
        System.out.println("we are eating together");
    }
    public void enjoy(){
        System.out.println("We are enjoying lots");
    }
    public static void main(String[] args) {
        ABCEmployeeRule abc = new  ABCEmployeeRule();
        FamilyRules father = new ABCEmployeeRule();//Dynamic Binding
        abc.maintainHour();
        abc.relocate();
        abc.report();
        abc.dress();
        father.eatTogether();
        father.enjoy();
        father.helpMembers();
        father.takeCareParents();
        System.out.println(EmloyeeRule.salary);
        System.out.println(EmloyeeRule.leaves);
    }
}
--------------------------------------------------------------------------------------------------------------------
Encapsulation

* Process of binding data and methods together into a Single unit.
--------------------------------------------------------------------------------------------------------------------
String,StringBuffer,StringBuilder
1,String Example
public class StringExample {
    public static void main(String[] args) {
        String name = "Agniprasath";
        int number = 3;
        //returns character value for the particular index
        System.out.println(name.charAt(1));
        //returns the string length
        System.out.println(name.length());
        //check the equality of string with the given object.
        System.out.println(name.equals("Arun"));
        //check the equality of string e=with the given string obj without case sensitivity.
        System.out.println(name.equalsIgnoreCase("AGANIPRASATH"));
        //Check if string is empty or not only answer true or false.
        System.out.println(name.isEmpty());
        //returns True or false based on the given value is present or not.
        System.out.println(name.contains("a"));
        //Take a particular portion of the string. imp being print pannum.
        System.out.println(name.substring(1));
        //Take a particular portion of the string being and end index. imp end print pannathu.ex tha code 3
        System.out.println(name.substring(1,3));
        //appends the String to the given char.imp name sekurathu.
        System.out.println(name.concat(" Arulprasath"));
        //replaces the existing char with give char. imp namku theva illatha name eduthu chage pannikalam.
        System.out.println(name.replace("A","a"));
        System.out.println(name.replace("Agni","riya"));
        //Find the position of char in string. A enna ijntex num nu print pannum.
        System.out.println(name.indexOf("A"));
        //Find the chat specified from the index position.
        System.out.println(name.indexOf("a",7));
        System.out.println(name.indexOf("sath",1));
        //Trim will remove the white spaces before and after.imp munadi pinadi iruka space remove pannum nadula irutha la remove pannathu
        System.out.println(name.trim());
        //convert the given data type to String.
        System.out.println(String.valueOf(number));
        //UpperCase and lowerCase.
        String upperCase = "RIYYAPARASNTH";
        System.out.println(upperCase.toLowerCase());
        String lowerCase = "agniprasath";
        System.out.println(lowerCase.toUpperCase());
        //Returns a joined String with Given delimiter
        System.out.println(String.join("-","learning","Automation","online"));
        System.out.println(String.join("/","30","05","1999"));
        //Split
        String splitThis="Am,I,teaching,Good?";
        String [] splittedWorlds = splitThis.split(",");
        for(String string: splittedWorlds){
            System.out.println(string);
        }}}
--------------------------------------------------------------------------------------------------------------------
2,StringBuffer Examples
public class StringBufferExamples {
    public static void main(String[] args) {
        System.out.println("String is Immutable");
        String name = "Arya";
        System.out.println("Appending name is Original :" + name.concat("prasath"));
        System.out.println("Original Name :"+name);
        System.out.println("******************************");
        System.out.println("String is mutable");
        StringBuffer name1 = new StringBuffer("Arya");
        System.out.println("Appending name is Original : " + name1.append("prasath"));
        //StringBuffer method
        //Reverse. imp string is don't have string Reverse method StringBuffer only reverse method.
        StringBuffer replaceThis = new StringBuffer("Arul");
        System.out.println(replaceThis.replace(0,3,"karthick"));
        //delete
        StringBuffer delete = new StringBuffer("xyzArul");
        System.out.println(delete.delete(0,3));
        //Insert
        StringBuffer insert = new StringBuffer("Moni");
        System.out.println(insert.insert(4,"sha"));
        //Capacity
        System.out.println(insert.capacity());
        //Like String we have charAt,Substring,length method as well
        StringBuffer uc = new StringBuffer("Moni");
        System.out.println(uc.charAt(0));//charAt
        System.out.println(uc.length());//length
        System.out.println(uc.substring(1,3));//Substring
}}
--------------------------------------------------------------------------------------------------------------------
3,StringBuilder Examples
public class StringBuilderExamples {
    public static void main(String[] args) {
        System.out.println("String is Immutable");
        String name = "Arya";
        System.out.println("Appending name is Original :" + name.concat("prasath"));
        System.out.println("Original Name :"+name);
        System.out.println("******************************");
        System.out.println("String is mutable");
        StringBuilder name1 = new StringBuilder("Arya");
        System.out.println("Appending name is Original : " + name1.append("prasath"));
        //StringBuilder method
        //Reverse. imp string is don't have string Reverse method StringBuffer only reverse method.
        StringBuilder replaceThis = new StringBuilder("Arul");
        System.out.println(replaceThis.replace(0,3,"karthick"));
        //delete
        StringBuilder delete = new StringBuilder("xyzArul");
        System.out.println(delete.delete(0,3));
        //Insert
        StringBuilder insert = new StringBuilder("Moni");
        System.out.println(insert.insert(4,"sha"));
        //Capacity
        System.out.println(insert.capacity());
        //Like String we have charAt,Substring,length method as well
        StringBuilder uc = new StringBuilder("Moni");
        System.out.println(uc.charAt(0));//charAt
        System.out.println(uc.length());//length
        System.out.println(uc.substring(1,3));//Substring
    }}
    --------------------------------------------------------------------------------------------------------------------
  Exception handling.
   * Exception is an undesirable or unexcepected event,which occures during the execution of a program i.e at runtime that disrupts the normal flow of the program's
     instractions.It can be handled by our program.
  Error.
   *Impossible to recover from error,Error are of Unchecked Type,happen at Run-time,Cause by the environment on which application is running.
  Exception.
   * Possible to recover from exception,It can be of checked or unchecked.Can happen at compile time & Runtime,Caused by application.
  
  Object ->Throwable ->Exception ->Error
  Exception Two Types.
Checked Exception
 * Exception whicjh are indicatred during the compile time are know as checked exception or compile time Exception.
UnCheckedException  
 * Exception which will happen during the execution of the program are Unchecked or run time Exception.
 -----------------------------------------------------------------------------------------------------------------------
public class CheckedException {
//It is called checked exception. all are compile
    String name;
  public static void main(String[] args) {
    System.out.println(name);
 }}
 -----------------------------------------------------------------------------------------------------------------------
 public class UncheckedException {
 static String name;
 // It is called unchecked exception.
   public static void main(String[] args) {
       System.out.println(name.length());// Error is NullPointerException.
    }
}
//try block aprm katipa catch block the irukannum.
-------------------------------------------------------------------------------------------------------------------------
NullPointerException,ArithmeticException,NumberFormatException,ArrayIndexOutOfBoundsException.

public class SampleException {
    public static void main(String[] args) {
       // String str = null;
      //  System.out.println(str.length());//NullPointerException
        //*ArithmeticException e arthimetic problem exc i am facing use this
        try {
            int a = 30,b = 0;
            int c = a/b;
            System.out.println("result = "+c);
        }catch (ArithmeticException e){
            System.out.println("Can't divide a number by zero");
        }//*NumberFormatException
        try{
            int num = Integer.parseInt("karthick");
            System.out.println(num);
        }catch (NumberFormatException e){
            System.out.println("Number Format exception");
        }
        try{
            int a []= new int [5];
            a[7]=9;
        }catch (ArrayIndexOutOfBoundsException e){
            System.out.println("array index out of bounds");
        }}}
-------------------------------------------------------------------------------------------------------------------------
Exception Handling methods.(try,catch,finally,throw,throws,)

1,Try. (Used to specify a block where we should place exception code.)

*NestedTry
public class NestedTry{
    public static void main(String[] args) {

        try{
            try{
                int num = Integer.parseInt("karthick");
                System.out.println(num);
            }catch (NumberFormatException e){
                System.out.println("Number Format exception");
            } try{
                int a []= new int [6];
                a[7]=9;
            }catch (Exception e){
                System.out.println("Handled");
            }
            System.out.println("other Statement");
        }
        catch(Exception e){
            System.out.println("handing and recovered");
        } } }
 -------------------------------------------------------------------------------------------------------------------------      
2,   catch. (Used to handling the exception.)

*OneTryBlockMultipleCatch
public class OneTryBlockMultipleCatch {
    public static void main(String[] args) {
        try{
            int a []= new int [5];
            a[7]=9;
        }
        catch (ArrayIndexOutOfBoundsException e){
            System.out.println("array index out of bounds");//This catch block handling the exception that why another catch block not executed
        }catch (Exception e){
            System.out.println("It is not execute");
        }
        System.out.println("other exception");
    }}

public class Finally {
    public static void main(String[] args) {
        try {
            int num = Integer.parseInt("karthick");
            System.out.println(num);
        }
        finally {
            System.out.println("Finally is always executed");
        }}}
-------------------------------------------------------------------------------------------------------------------------
3,   Finally. (Used to execute the important code of the program.)
* Finally
public class Finally {
    public static void main(String[] args) {
        try {
            int num = Integer.parseInt("karthick");
            System.out.println(num);
        }
        finally {
            System.out.println("Finally is always executed");
        }}}
-------------------------------------------------------------------------------------------------------------------------
4,   Throw.   (Used to throw an exception.) (method la tha exception throw pannum)

* Throw
public class ThrowException {
    static void avg(){
        try{
            throw new ArithmeticException("demo");
        }catch (ArithmeticException e){
            System.out.println("Exception caught");
        }
    }
    public static void main(String[] args) {
        avg();
    }}
-------------------------------------------------------------------------------------------------------------------------
5,   Throws.   (Used to declare exceptions.)(method la tha exception throw pannum)
* Throws
public class ThrowException {
  /*  static void avg(){
        try{
            throw new ArithmeticException("demo");
        }catch (ArithmeticException e){
            System.out.println("Exception caught");
        }
    }
    public static void main(String[] args) {
        avg();
    }*///Like as throw but lit bit difference in code
  static void avg() throws ArithmeticException{
      System.out.println("inside avg function");
      throw new ArithmeticException("demo");
  }
    public static void main(String[] args) {
        try{
            avg();
        }finally {
            System.out.println("caught");
        }}}
-------------------------------------------------------------------------------------------------------------------------
* User define Exeption.(User can also create exception the user defind exception)

public class SampleUserdefine {
    //Throw

    public static void main(String[] args) {
        try{
            throw new Myexception(5);
        }catch (Exception e){
            System.out.println(e);
        }
    }
}
class Myexception extends Exception{
    int a;
    Myexception(int b){
        a=b;
    }
    public String toString(){
        return ("Exception number = "+a);
    }}
-------------------------------------------------------------------------------------------------------------------------
* Custom Exception.
import com.sun.security.jgss.GSSUtil;
import java.util.Scanner;
public class SampleCustom {
     static void validateInput(int number) throws InvalidInputException{
        if (number > 100){
            throw new InvalidInputException("Exception");
        }
        System.out.println("Valid Input");
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter a number less than 100 : ");
        int number = scanner.nextInt();
        try{
            validateInput(number);
        }catch (InvalidInputException e){
            System.out.println("caught Exception - Input is greater than 100");
        }

    }
}
class InvalidInputException extends Exception{
    InvalidInputException(String exceptionText){
        super(exceptionText);
    }
}
-------------------------------------------------------------------------------------------------------------------------
* SimpleDateFormat

import java.text.ParseException;
import java.text.SimpleDateFormat;
import java.util.*;
public class SampleDateFormat {
    static void convertDateFormate (String inputDate){
       try{
           SimpleDateFormat sdf = new SimpleDateFormat("dd/mm/yyyy");
           Date date = sdf.parse(inputDate);
           SimpleDateFormat outputsdf = new SimpleDateFormat("yyyy-mm-dd");
           String outputDate = outputsdf.format(date);
           System.out.println("After changing date format to yyyy/mm/dd : "+outputDate);
       } catch (java.text.ParseException e){
           System.out.println("Some error Occure while converting date formats. Exception is "+e);
       }
       }
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter date in dd/mm/yyyy format: ");
        String inputDate = scanner.nextLine();
        convertDateFormate(inputDate);
    }}
-------------------------------------------------------------------------------------------------------------------------
* TryCatchFinaly

public class TryCatchFinaly {

    public static void main(String[] args) {
        try {
            System.out.println("Inside try block");
           throw new Exception();
        }catch (Exception e){
           System.out.println("Inside Catch block");
        }finally {
            System.out.println("Inside finally block");
        }}
-------------------------------------------------------------------------------------------------------------------------------
Java Collection framwork:
  * interable -> iterator -> iterator<e> -> collection.
 List:
   * ArrayList
   * LinkedList
   * Stack(lagacy class)
   * Vector(lagacy class)
    
 Set:
   * Hashset
   * Linkedhashset
   * Treeset
    
It is not a true collection.
    
Map:
   * HashMap
   * HashLinkedMap
   * HashTable
   * TreeMap
--------------------------------------------------------------------------------------------------------------------------------
  (1)  List:
 1,   ArrayList.
    
      public class ArrayListExample<S> {
    /**
     * List(I) is the Child of Collection(I).
     * ArrayList (C) is one of the classes provides implementation for the List(I).
     * In list duplicate values are allowed and the insertion order is maintained.
     * The underlying DS is resizeable Array or Growable Array. We can insert Heterogeneous objects as well.
     * NOTE: All the collections can store Heterogeneous objects can be stored except TREE SET and TREE MAP.
     * ArrayList and vector implements RandomAccess, Serializable and Cloneable Interfaces
     * Synchronized-> No
     * Thread safe-> NO
     * Default capacity-10
     * <p>
     * Fill Ratio or Load factor:1 or 100%
     * Growth Rate: current_size + current_size/2
     */
    public void arrayListExamle() {
     /*    List<Integer> arrayList = new ArrayList<Integer>();
        arrayList.add(5);
        arrayList.add(4);
        arrayList.add(3);
        arrayList.add(2);
        arrayList.add(1);
        ListIterator<Integer> iterator = arrayList.listIterator();
        while (iterator.hasNext()){
            System.out.println(iterator.next());
        }
        System.out.println("**************************");
        while (iterator.hasPrevious()){
            System.out.println(iterator.previous());
        }*/
        List<String> arrayList = new ArrayList<String>();
        arrayList.add("Bugatti");
        arrayList.add("Benz");
        arrayList.add("BMW");
        arrayList.add("Bugatti");
        arrayList.add("Bentley");
        System.out.println(arrayList);
        System.out.println(arrayList.get(1));//get enrathu index num kadupidikala
        System.out.println(arrayList.indexOf("kart"));//indexOf la illa peru kudutha -1 nu print akum
        System.out.println(arrayList.indexOf("Bugatti"));//indexOf use panna first atha name enga varutho atha index kudukum
        System.out.println(arrayList.lastIndexOf("Bugatti"));//lastIndexOf use last la iruthu etha index la varuthu nu chk pannum
        System.out.println(arrayList);
        List<String> anotherList = new ArrayList<String>();//duplication
        anotherList.addAll(arrayList);
        anotherList.clear();//Clear use panna ellathaium clear pannalam
        System.out.println(anotherList);
        arrayList.remove(0);//index num remove pannna la
        System.out.println(arrayList);//
        arrayList.remove("Bugatti");//String name remove pannalam
        System.out.println(arrayList);
        arrayList.add(null);//array list la null enra element add panna mudium.
        System.out.println(arrayList);
        arrayList.set(0, "karthi");// set using the change the char and any thing
        System.out.println(arrayList);
        System.out.println(arrayList.isEmpty());// ArrayList is value iruka illlaiya nu kekurathu true or false
        System.out.println(arrayList.size());
        //iterate
        System.out.println("*for each loop*");
        for (String string : arrayList) {
            System.out.println(string);
        }
        System.out.println("*for each loop*");
        for (int i = 0; i < arrayList.size(); i++) {//.aprm size use pannanum
            System.out.println(arrayList.get(i));//.aprm get use pannanum
        }
        System.out.println("--------------------------------------");
        //ListIterator frd direction and reverse direction two things are possible.
        ListIterator<String> iterator = arrayList.listIterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
        System.out.println("-------------------------------------------");

        while (iterator.hasPrevious()) {
            System.out.println(iterator.previous());
        }
        System.out.println("-----------------------------------------");
        //iterator only frwd direction only possible
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
    }

    public static void main(String[] args) {
        ArrayListExample example = new ArrayListExample();
        example.arrayListExamle();
    }}
--------------------------------------------------------------------------------------------------------------------------------
 2,   LinkedList.
    
    import java.util.Iterator;
    import java.util.LinkedList;

public class LinkedListExample {
            /**
             * LinkedList is implemented using Doubly linked list. This is best suited for insertion and deletion operations.
             * Unlike ArrayList, this is not the best for retrieving the data.
             * All the collections implements Serializable and cloneable Interfaces.
             * LinkedList also implements those Interfaces but not RandomAccess Interface.
             */
            public void linkedListOperationsExample() {
        //Create a simple Linked list
                LinkedList<Integer> linkedList = new LinkedList<Integer>();
                linkedList.add(2);
                linkedList.add(3);
                linkedList.add(4);
                System.out.println("Linked List :"+ linkedList);
                //Add an element to the first position
                linkedList.addFirst(1);// mutha oru num add panna
                System.out.println("Linked List after adding first:"+ linkedList);
                //Add an element at last
                linkedList.addLast(5);//last la oru num add panna
                System.out.println("Linked List after adding last:"+ linkedList);
                /*
                 * LinkedList performs the worst if the operation is retrieval of data.
                 * Hence if our requirement is to fetch data, we should use ArrayList.
                 * But LinkedList is the best choice if we have requirements of adding and
                 * removing data very often. In this case we should avoid ArrayList
                 */
                //Get the first value
                System.out.println("First Value :" +linkedList.getFirst());//o index print pannum
    
                //Get the first value using index position
                System.out.println("First Value using index :"+linkedList.get(0));// what is index num you give print it.
    
                /*
                 * Now get the third value of the list.
                 * Since LinkedList has the data structure of doubly linked list,
                 * the value of the third index is known only to the link present in
                 * the Second index. Internally, the program will traverse to index number 2 and then only
                 * it can get the value of 3. So Linked list is not suited for search operations.
                 */
                System.out.println("Third value of the list : "+ linkedList.get(3));//for ex you 3 index num print it 4
                //update the values using set().
                //Integer newFirst=linkedList.get(0);
                //linkedList.set(0, newFirst);
                //System.err.println("After 0th position updated :"+linkedList);
    
                //removeFirst and removeLast
                System.out.println("Remove first :"+linkedList.removeFirst());
                System.out.println(linkedList);
                System.out.println("Remove last :"+linkedList.removeLast());
                System.out.println(linkedList);
                //poll method  and pollfirst() deletes the first element in the list
                System.out.println(linkedList.poll());
                System.out.println(linkedList);
                //pollLast deletes the last
                linkedList.pollLast();
                System.out.println(linkedList);
                //Adding
                linkedList.addFirst(1);
                linkedList.add(2);
                linkedList.add(3);
                linkedList.add(4);
                linkedList.add(5);
                linkedList.add(6);
                //removeFirstOccurence
                linkedList.removeFirstOccurrence(2);
                System.out.println("After removing the first occurence of 2 "+ linkedList );
                //removeLastOccurrence
                linkedList.removeLastOccurrence(6);
                System.out.println("After removing the last occurence of 6 "+ linkedList );
                System.out.println("-----------------------------------------------------");
            }/*
             * Iteration of Linked List with simple for loop
             */
            public void iterateLinkedListWithSimpleFor() {
    
                LinkedList<String> linkedList = new LinkedList<String>();
                linkedList.add("a");
                linkedList.add("b");
                linkedList.add("c");
                linkedList.add("d");
                System.out.println("Simple For loop");
                for (int index = 0; index < linkedList.size(); index++) {
                    System.out.println("Elements in the LL are " + linkedList.get(index));
    
                }
            }/*
             * Iteration of Linked List with Advanced For loop (For each)
             */
    
            public void iterationWithAdvancedFor(){
                LinkedList< String> linkedList= new LinkedList<String>();
                linkedList.add("a");
                linkedList.add("b");
                linkedList.add("c");
                linkedList.add("d");
                System.out.println("For Each");
                for (String string : linkedList) {
                    System.out.println("Elements in the LL are "+ string);
                }
                System.out.println("-----------------------------------------------------");
            }/*
             * Iterate using While
             */
            public void iterateUsingWhile(){
                LinkedList< String> linkedList= new LinkedList<String>();
                linkedList.add("a");
                linkedList.add("b");
                linkedList.add("c");
                linkedList.add("d");
                int number=0;
                System.out.println("While");
                while(linkedList.size()>number){
                    System.out.println("Elements in the LL are "+ linkedList.get(number));
                    number++;
                }
                System.out.println("-----------------------------------------------------");
            }/*
             * Iterate using Iterator
             */
            public void iterateUsingIterator(){
                LinkedList< String> linkedList= new LinkedList<String>();
                linkedList.add("a");
                linkedList.add("b");
                linkedList.add("c");
                linkedList.add("d");
                Iterator<String> iterator = linkedList.iterator();
                System.out.println("Iterator");
                while(iterator.hasNext()){
                    System.out.println("Elements in the LL are "+ iterator.next());
                }
                System.out.println("-----------------------------------------------------");
            }
    
    
            public static void main(String[] args) {
                LinkedListExample linkedListExample = new LinkedListExample();
                linkedListExample.linkedListOperationsExample();
                linkedListExample.iterateLinkedListWithSimpleFor();
                linkedListExample.iterationWithAdvancedFor();
                linkedListExample.iterateUsingWhile();
                linkedListExample.iterateUsingIterator();
            }}
   --------------------------------------------------------------------------------------------------------------------------------  
 (2)   Set:
    
  1, Hashset:
    
    import java.util.HashSet;
import java.util.Iterator;

public  class HashSetExample {
    /**
     * Set(I)-> HashSet (C) and LinkedHashSet(C) are implementations
     * Set(I) -> SortedSet(Child Interface)->NavigableSet(I)=> TreeSet(C) is the implementation
     * Important points to remember:
     * 1. To store group of individual objects.
     * 2. Duplicates not allowed
     * 3.Insertion order will not be maintained
     * 4.Set(I) doesn't have any new methods other than given in Collection(I).
     * 5. DS for HashSet is Hash table
     * 6. If we add duplicate value to HashSet, simply it will return false to the
     * add() and it won't throw any error or exception.
     * 7. We can insert null values
     * 8. Heterogeneous values can be added.
     * 9. Implements Serializable and Cloneable?-> Yes
     * 10. Data are stored based on hashcode, so search is very effective.
     * 11. Fill Ratio or Load factor:0.75 or 75%
     * 12.Default capacity-16
     */
    /*
     * Number Constructors available in HashSet=4
     * 1. HashSet hs= new HashSet();// size-16 and fill ratio is 0.75
     * 2. HashSet hs= new HashSet(int initialSize);size as declared and fill ratio is 0.75(default)
     * 3. HashSet hs= new HashSet(int initialSize, float fillRatio);//size and fill ratio can be declared
     * 4. HashSet hs= new HashSet(Collection c);// creates a HashSet for any given Collection (Acts as interconversion)
     */
    public void basicExamplesHashSet() {
        HashSet<String> hashSet = new HashSet<String>();
        hashSet.add("A");
        hashSet.add("D");
        hashSet.add("E");
        hashSet.add("F");
        hashSet.add("A"); // the return type of add() is boolean. Since A is already there it will return false and wont add
        hashSet.add(null);
        //We have no control on insertion order
        System.out.println("Contents of the HashSet :" + hashSet);
    }
    /*
     * Iterate using Iterator
     */
    public void iterateUsingIterator() {
        HashSet<String> hashSet = new HashSet<String>();
        hashSet.add("A");
        hashSet.add("D");
        hashSet.add("E");
        hashSet.add("F");
        hashSet.add("A");

        Iterator<String> iterator = hashSet.iterator();
        while (iterator.hasNext()) {
    
            System.out.println("Elements of HashSet :" + iterator.next());
        }
    }
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        HashSetExample hashSetExample = new HashSetExample();
        hashSetExample.basicExamplesHashSet();
        hashSetExample.iterateUsingIterator();
    }}
--------------------------------------------------------------------------------------------------------------------------------    
2, LinkedHashSet:
    
    import java.util.LinkedHashSet;

public class LinkedHashSetExample {
    /**
     * LinkedHashSet->Child class of HashSet
     * DS-> Hash table + Linked List
     * Insertion order is preserved
     * Duplicates not allowed
     */
    public void linkedHashSetExample(){
        LinkedHashSet linkedHashSet = new LinkedHashSet();
        linkedHashSet.add(1);
        linkedHashSet.add("A");
        linkedHashSet.add("B");
        linkedHashSet.add("C");
        linkedHashSet.add("10");
        linkedHashSet.remove("10");
        System.out.println("Insertion Order preserved Linked Hash Set :"+ linkedHashSet);
    }
    public static void main(String[] args) {
        // TODO Auto-generated method stub
        LinkedHashSetExample example= new LinkedHashSetExample();
        example.linkedHashSetExample();
    }}
--------------------------------------------------------------------------------------------------------------------------------
3, TreeSet  
  import java.util.Iterator;
import java.util.TreeSet;

public class treeSetExample {

    public static void treesetExample() {
        //Creating object
        TreeSet<Integer> treeSet = new TreeSet<Integer>();
        treeSet.add(10);
        treeSet.add(1);
        treeSet.add(2);
        treeSet.add(9);
        treeSet.add(7);
        treeSet.add(3);
        System.out.println(treeSet);
        System.out.println("Elements are sorted on ascending order :" + treeSet);
        //first()
        System.out.println("First element :" + treeSet.first());//first letter print pannum
        //last()
        System.out.println("Last element :" + treeSet.last());//last letter print pannum
        //headSet()
        System.out.println("Values lesser than given value" + treeSet.headSet(3));//etha value nama kudukuromo atha value kella irukuratha mattum tha print pannum then aha num varathu
        //tailSet()
        System.out.println("Values equal to and higher than given value"+treeSet.tailSet(9));//entha range solluromo athu ku mela iruka value print pannum na soolura num sethu print pannum
        //subSet()
        System.out.println("Subset values :"+treeSet.subSet(2, 9));//etha range solluromo ethu kula iruka value print pnnum and last nama kudutha value ya print pannathu
        //comparator()
        System.out.println("Comparator returns null if the sorting is default natural order :"+ treeSet.comparator());
        //Adding null to a non empty tree set causes null pointer excpetion
        //treeSet.add(null);
        /*null can be easily added if the tree set is empty. If there are any elements present, the
         * comparator will check for the sorting order between the previosly added element and
         * the null. Since it compares null with the objects exisiting we are getting NPE.
         * Same is the case, if we add null first and add other elements, NPE will happen.
         */
        System.out.println("Higher: "+treeSet.higher(3));//etha value kudukuromo atha vda periya value sollum
        System.out.println("Higher: "+treeSet.lower(3));//etha value kudukuromo atha vda sena value sollum
        System.out.println("Poll last; "+treeSet.pollFirst());//first value
        System.out.println("Poll last; "+treeSet.pollLast());//last value
        System.out.println("After polling : "+treeSet);//first value and last value remove pannu after irukuratha print pannum
        System.out.println("Deserding order: "+treeSet.descendingSet());
        //iterate
        System.out.println("Ascending order");
        Iterator<Integer> iterator = treeSet.iterator();
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
        System.out.println("Descending order");
        Iterator<Integer> descIterator = treeSet.descendingIterator();
        while (descIterator.hasNext()){
            System.out.println(descIterator.next());
        }
    }
    public static void main(String[] args) {
        treeSetExample.treesetExample();
    }}
--------------------------------------------------------------------------------------------------------------------------------   
It is not collection part.
1,   Map:
 1,     HashMap:
    
    import java.util.HashMap;
    import java.util.Map;
public class HashMapExample {
    public static void main(String[] args) {
        HashMap<Integer,String> employeeMap = new HashMap<Integer,String>();
        //insert an element PUT method use
        employeeMap.put(1,"agni");
        employeeMap.put(2,"Riya");
        employeeMap.put(3,"Arya");
        employeeMap.put(4,"Mani");
        employeeMap.put(5,"Duck");
        System.out.println("employeeMap " +employeeMap);
        //to Make a copy of the map contain
        Map<Integer,String> duplicateMap = new HashMap<Integer,String>();
        duplicateMap.putAll(employeeMap);
        System.out.println("duplicateMap "+duplicateMap);
        //Clear to delete the map content
        duplicateMap.clear();
        System.out.println(duplicateMap);
        //To check the key is present or not in map
        System.out.println("Does this ma has key 1? "+employeeMap.containsKey(1));
        //To check the value is present or not in map
        System.out.println("Does this ma has value Duck? "+employeeMap.containsValue("Duck"));
        //clone the map
        System.out.println("clone the map "+employeeMap.clone());
        //check if the map is empty or not
        System.out.println("Is empty "+employeeMap.isEmpty());
        //fetch the set of key in the ( note : here it's not list of keys,it's set of keys.
        //Because List will allow duplicate but set won't. keys should be Unique.
        System.out.println("Key set "+employeeMap.keySet());
        //fatch a value
        System.out.println(employeeMap.get(1));
        //fatch all value
        System.out.println("All values "+employeeMap.values());
        //entry set
        System.out.println(employeeMap.entrySet());
    }
}
 --------------------------------------------------------------------------------------------------------------------------------
2,  HashLinkedMap  
    
    import java.util.HashMap;
    import java.util.LinkedHashMap;

public class LinkedHashMapExample {
    public static void main(String[] args) {
        LinkedHashMap<String,String> heros = new LinkedHashMap<String,String>();
        //Linked hash map is like as Hashmap methods every thing should be same
        //only difference LinkedHashMap maintained the preserved order.
        heros.put("karthick","mani");
        heros.put("palani","prabha");
        heros.put("sethu","priya");
        System.out.println(heros);
        System.out.println("**This the difference **");
        HashMap<String,String> heros1 = new HashMap<String,String>();
        heros1.put("karthick","mani");
        heros1.put("palani","prabha");
        heros1.put("sethu","priya");
        heros1.put("tamil","gopi");
        System.out.println(heros1);
    }}
--------------------------------------------------------------------------------------------------------------------------------
3,    TreeMap.
    
    import java.util.TreeMap;

public class TreeMapExample {
    public static void main(String[] args) {
        //null insertion not main
        TreeMap<String,String> placesInTrichy = new TreeMap<String,String>();
        placesInTrichy.put("chennai","mathurai");
        placesInTrichy.put("mathurai","mathurai");
        placesInTrichy.put("thiruthani","mathurai");
        placesInTrichy.put("thirupathi","mathurai");
        System.out.println(placesInTrichy);
    }}
----------------------------------------------------------------------------------------------------------------------------------


























































































































  
  
  
  
  
  
    






































































