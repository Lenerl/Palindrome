# Palindrome

//You can enter numbers between 1 and 9999 here, and my program will tell you if your number is a palindrome.
// A palindrome is a number that you start reading from the front or back and it stays the same.:)

public class Main {

    public static void main(String[] args) {
        System.out.println("1221"+"is a " + isPalindrome(1221) + " Palindrome");
        System.out.println("121"+"is a " + isPalindrome(121) + " Palindrome");
        System.out.println("1"+"is a " + isPalindrome(1) + " Palindrome");
        System.out.println("55"+"is a " + isPalindrome(55) + " Palindrome");
        System.out.println("123"+"is a " + isPalindrome(123) + " Palindrome");

    }

    public static boolean isPalindrome(int number) {
        if(number>=1 && number <10){
            return true;
        }
        if(number>10 && number < 100){
            if(number%10 == number/10){
                return true;
            }
        }
        if(number > 100 && number < 1000){
            if((number%100)%10 == number/100){
                return true;
            }
        }
        if(number >1000 && number <10000){
            int x = (number-(number/1000)*1000); //221
             // tausender                einer            hunderter                          zehner
            if(((number%1000)%100)%10 == number/1000 && ((number-(number/1000)*1000)/100) == (x-(x/100)*100)/10){
                return true;
            }
        }
        return false;


    }
}






