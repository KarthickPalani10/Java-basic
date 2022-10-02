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
    }
}
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
    }
}
-------------------------------------------------------------------------------------------














































































































































































