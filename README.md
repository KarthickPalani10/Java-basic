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
  Exception
   *Impossible to recover from error,Error are of Unchecked Type,happen at Run-time,Cause by the environment on which application is running.
  Error.
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
//try block aprm katipa catch block the irukannum..
-------------------------------------------------------------------------------------------------------------------------


























































































  
  
  
  
  
  
    






































































