# BracU-CSE110-2026
<br>
<H2><u>Assignment - 1</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2001-%20Introduction%20to%20Flowcharts%20and%20Java%20Programming.pdf" target="_blank">Questions</a></H4>
  <H4>Solutions</H4>
  
```
//answer to question 1
public class answer1 {
    public static void main(String[]args) {
        int minutes = 3456789;
        int days = ((minutes/(60*24))%365);
        int year = ((minutes/(60*24))/365);

        System.out.println(year + " years " + days + " days");
    }
}



//answer to question 2
public class answer2{
    public static void main (String[]args){
        int a = 2;
        int b = 5;
        int c = 8;
        int d = ((((c-a)/3)*2*b)+7);

        System.out.println("Answer: " + d);
    }
}



//answer to question 3
public class answer3 {
    public static void main (String[]args){
        int id = 1000054943;
        int x = id%10;
        int y = id%100;

        System.out.print(x);
        System.out.print(y/10);
    }
}



//answer to question 4
public class answer4{
    public void main (String[]args){
        int length = 10;
        int width = 13;
        double diagonal = Math.sqrt(length*length + width*width);

        System.out.println("Diagonal distance = " + diagonal);
    }
}



//answer to question 5
public class answer5{
    public void main (String[]agrs){
        double a = 4.5;
        double b = 9.5;
        double c = Math.sqrt(a*a + b*b);

        System.out.println("SinA = " + a/c);
        System.out.println("CosA = " + b/c);
        System.out.println("SinB = " + b/c);
        System.out.println("CosB = " + a/c);
    }
}
```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass1.pdf" target="_blank">Tracing</a></H4>

  
<H2><u>Assignment - 2</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2002-%20Branching.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task1
import java.util.Scanner;
public class question1 {
    public static void main (String [] args){

        Scanner Sc1 = new Scanner(System.in);
        
        int x = Sc1.nextInt();

        if(x%5==0 && x%7==0){
            System.out.println("Invalid: Divisible by both");
            }
        else if(x%7==0){
            System.out.println("Divisible by 7 Only");
            }
        else if (x%5==0){
            System.out.println("Divisible by 5 Only");
            }
        else {
            System.out.println("No");
        }
    }
    }



//task2
import java.util.Scanner;
public class question2 {
    public static void main (String [] agrs){
        Scanner age = new Scanner(System.in);
        Scanner kwh = new Scanner(System.in);

        int charge = 15;
        int x = age.nextInt();
        double y = kwh.nextDouble();
        double bill = charge*y;
        double totalbill =0;
          
    if(y<=100){
        if(x<18){ totalbill = (bill-bill*0.2);
        }
        else if(x>=18 && x<=60){ totalbill = bill;
        }
        else if(x>60){ totalbill =(bill-bill*0.1);
        }
        System.out.println("Final Bill: " + totalbill + " Taka");
    }
    else if(y>100){
        if(x<18){ totalbill = (bill-bill*0.2);
        }
        else if(x>=18 && x<=60){ totalbill = bill;
        }
        else if(x>60){ totalbill =(bill-bill*0.1);
        }
        System.out.println("Final Bill: " + (totalbill+totalbill*0.05) + " Taka");
    }
}
}



//task3
import java.util.Scanner;
public class question3 {
    public static void main (String [] args) {
        Scanner sc1 = new Scanner(System.in);
        Scanner sc2 = new Scanner(System.in);
        Scanner sc3 = new Scanner(System.in);
  
  float num1 = sc1.nextFloat();
  float num2 = sc2.nextFloat();
  float num3 = sc3.nextFloat();
  
if(num1 > num2 && num1 > num3){
    System.out.println("Maximum number is " + num1);
    }
else if(num2 > num1 && num2 > num3){
    System.out.println("Maximum number is " + num2);
    }
else{
    System.out.println("Maximum number is " + num3);
}
if(num1 < num2 && num1 < num3){
    System.out.println("Minimum number is " + num1);
    }
else if(num2 < num1 && num2 < num3){
    System.out.println("Minimum number is " + num2);
    }
else{
    System.out.println("Minimum number is " + num3);
}

  }
  }



//task4
import java.util.Scanner;
public class question4 {
    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner(System.in);
        Scanner Sc2 = new Scanner(System.in);
        Scanner Sc3 = new Scanner(System.in);

        int x = Sc1.nextInt();
        int y = Sc2.nextInt();
        int z = Sc3.nextInt();

        if((x==y && y==z) && x==z){
            System.out.println("This is a Equilateral triangle");
        }
        else if((x==y || y==z) || x==z){
            System.out.println("This is a Isosceles triangle");
        }
        else if((x!=y && y!=z) && x!=z){
            System.out.println("This is a Scalene triangle");
            }
        } 
    }
    




//task5
import java.util.Scanner;
public class question5 {
    public static void main (String [] agrs){

    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);

    int toPay = Sc1.nextInt();
    int given = Sc2.nextInt();

    //Notes: 100, 50, 20, 10
    //Coins: 5, 2, 1

    if(given > toPay){
        int change = given - toPay;
        System.out.println("The returned amount is " + change + " taka.");

        int notes100        = change / 100;
        int remainAfter100  = change % 100;
        
        int notes50         = remainAfter100 / 50;
        int remainAfter50   = remainAfter100 % 50;

        int notes20         = remainAfter50 / 20;
        int remainAfter20   = remainAfter50 % 20;

        int notes10         = remainAfter20 / 10;
        int remainAfter10   = remainAfter20 % 10;

        int coin5           = remainAfter10 / 5;
        int remainAfter5    = remainAfter10 % 5;
        
        int coin2           = remainAfter5 / 2;
        int remainAfter2    = remainAfter5 % 2;

        System.out.println("100 taka note: " + notes100);
        System.out.println("50 taka note: " + notes50);
        System.out.println("20 taka note: " + notes20);
        System.out.println("10 taka note: " + notes10);
        System.out.println("5 taka coin: " + coin5);
        System.out.println("2 taka coin: " + coin2);
        System.out.println("1 taka coin: " + remainAfter2);
    }
    else if (given < toPay){
        int due = toPay - given;
        System.out.println("Please pay " + due + " taka more.");
    }
    else{
        System.out.println("The returned amount is 0 taka.");
    }

}
}



//task6
import java.util.Scanner;
public class question6 {
    public static void main (String [] agrs){

        Scanner Sc1 = new Scanner(System.in);
        Scanner Sc2 = new Scanner(System.in);
        Scanner Sc3 = new Scanner(System.in);

        int a = Sc1.nextInt();
        int b = Sc2.nextInt();
        int c = Sc3.nextInt();

        if((a==b && b==c) && a==c){
            System.out.println("All numbers are equal");
        }
        else if((a!=b && b!=c) && a!=c){
            System.out.println("All numbers are different");
        }
        else{
            System.out.println("Neither all are equal nor different");
        }

    }
    
}
```
<H4><a href =""https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass2.pdf>Tracing</a></H4>



<H2><u>Assignment - 3</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2003-%20Linear%20Loops.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task1
import java.util.Scanner;
public class question1{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    int n = Sc1.nextInt();
    int i = 0;
    
      for(i=0;i<=n;i+=1){
        if(i%5==0 && i%3!=0){
        System.out.println(i);
        }
      }
  }
}


//task2
import java.util.Scanner;
public class question2{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
    
    int H = Sc1.nextInt();
    int C = Sc2.nextInt();
    int count = 0;

    for(count = 1; H>=3 && C>=2; count+=1){
      H = H-3;
      C = C-2;
      System.out.println("Potion-"+count+" created");
      System.out.println("Remaining Herbs:"+H+", Remaining Crystals:"+C);
    
    }
    count = count -1;
    System.out.println("Potions Created: "+ count);
    if(count%2==0){
    System.out.println("Stable Elixir");
    }
    else {
    System.out.println("Volatile Brew");
    }
  }
  }
  


//task3
import java.util.Scanner;
public class question3{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
    Scanner Sc3 = new Scanner(System.in);
    
    int E; //energy
    int N; //no. of river
    int D; //distance of river
    int count = 1;
 
    System.out.print("Energy (E): ");
    E = Sc1.nextInt();
    
    System.out.print("Number of River (N): "); 
    N = Sc2.nextInt();
    
    for(count = 1; count <= N; count++){
    System.out.print("Enter River Distance D"+count+": "); 
    D = Sc3.nextInt();
    
    if(D>5){
    E = E-(D/2);
    }
    else if(D<=5){
    E = E-2;
    }
    if(E<0){
    System.out.println("Tired at River "+count);
    break;
    }
    
    }
    
    if(E>=0){ 
    System.out.println("All Done");
    System.out.println(E+" energy left");
    } 
  }
}



//task4
import java.util.Scanner;

public class question4{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    int x = Sc1.nextInt(); 
    int y =1;
    int z =1;
    int i = 0;
    
    if(x<0){
    z = (-1)*x;
    }
    else{
    z = x;
    }
    for(i = 1; z>0; i+=1){
     y = z%10; 
     z = z/10; 
     
     if(z>0){
     System.out.print(y + ", ");
    }
     else if (z<=0 && x>0){
     System.out.print(y); //if the value is positive
     }
     else if (z<=0 && x<0){
     System.out.print(y + ", -"); //if the value is negative
     }
    }
}
}


//task5
import java.util.Scanner;
public class question5{
  public static void main (String [] agrs){
  
  Scanner Sc1 = new Scanner (System.in);
  
  System.out.print("Enter the N-digit vault code:");
  int n = Sc1.nextInt();
  
  int count = 1;
  int x = n;
  int y = 0;
  int power = 1;

  for(count = 0; x>0; count+=1){
  x = x/10;
  }
  
  for(int i = 1; i<count; i+=1){
  power = 10*power;
  }

  for(int j = 1; j<=count; j+=1){
  y = (n/power);
  n = n%power;
  System.out.print(y + ", ");
  power = (power/10);
  }

  }
}


//task6
import java.util.Scanner;

public class question6{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    int n = Sc1.nextInt(); 
    int i = 1;
    int sum = 0;

    if(n%2==0 && n!=2){
    System.out.println(n + " is not a prime number");
    for(i = 1; i<=n/2; i+=1){   
      if(n%i==0){  
        sum = sum+i; 
      }
    }
     if(sum==n){
     System.out.println(n + " is a perfect number");
     }
     else{
     System.out.println(n + " is not a perfect number");
     }
    }
    
    else if(n!=1){
    System.out.println(n + " is a prime number");
    System.out.println(n + " is not a perfect number");
    }
    
    else{
    System.out.println(n + " is a unique number");
    } 
  }
}


//task7
public class question7{
  public static void main (String [] agrs){
  int sum = 0;
    
    for(int i=1; i<=600; i+=1){
      if((i%7==0 || i%9==0) && !(i%7==0 && i%9==0)){
        sum = sum+i;
        }
      }
    System.out.println(sum);
  }
}


//task8
import java.util.Scanner;

public class question8{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    int i = 0;
    int j = 0;
    int k = 0;
    
    System.out.print("Enter an integer: ");
    int x = Sc1.nextInt();
    
    for(i=1; i<=x; i++){
    System.out.print("Enter number"+i+": ");
    int y = Sc1.nextInt();
    
    if(y>=0){
      j = j+1;
    }
    else{
      k = k+1;
    }
    }
    System.out.println(j+" Non-negative Numbers");
    System.out.println(k+" Negative Numbers");
    
  }
}

```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass3.pdf">Tracing</a></H4>



<H2><u>Assignment - 4</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2004-%20Nested%20Loops.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task1
import java.util.Scanner;

public class task1{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
    
    System.out.print("Enter a starting number:");
    int x = Sc1.nextInt();
    System.out.print("Enter an ending number:");
    int y = Sc2.nextInt();
    
    int i = 0;
    int j = 0;
    int k = 0;
    int sum = 0;
    int count=0;
    
    for(i = 0; x<=y; i+=1){
      for(j = x; j>0; j = j/10){
        count=count+1;
      }
      for(j = x; j>0; j = j/10){
        k = j%10;
        sum += Math.pow(k, count);
      }
      if(sum==x){
        System.out.println(x + " is an armstrong number");
      }
    x=x+1;
    count = 0;
    sum=0;
    }
  }
}



//task2
import java.util.Scanner;

public class task2{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
    
    System.out.print("Enter the number of students to check: ");
    int x = Sc1.nextInt();
    
    for(int i = 1; i<=x; i++){
    System.out.print("Enter Student ID: ");
    int y = Sc2.nextInt();
    int j = y;
    for(j = y; j%2==0; j=j/2){
      //System.out.println(y + " is a power of 2");
    }
    if(j==1){
      System.out.println("Lucky ID");
    }
    else{
      System.out.println("Not Lucky");
    }
    }
  }
}



//task3
import java.util.Scanner;

public class task3{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
//    Scanner Sc3 = new Scanner(System.in);
//    Scanner Sc4 = new Scanner(System.in);
    
    System.out.print("Enter number of days: ");
    int days = Sc1.nextInt();
    
    int sum = 0;
    
    for(int i = 1; days>=i; i+=1){
      System.out.println("Enter Sales for Day "+i);
      for(int j = 1; 3>=j; j+=1){
        int product = Sc2.nextInt();
        sum = sum+product;
      }
      if(sum>=100 && sum<200){
        double withTax = (sum*0.02)+sum;
        System.out.println("Day "+i+": Total Sales with Tax: "+withTax);
      }
      else if(sum>=200 && sum<500){
        double withTax = (sum*0.05)+sum;
        System.out.println("Day "+i+": Total Sales with Tax: "+withTax);
      }
      else if(sum>=500){
        double withTax = (sum*0.1)+sum;
        System.out.println("Day "+i+": Total Sales with Tax: "+withTax);
      }
      else if(sum<100){
        double withTax = (sum*0.0)+sum;
        System.out.println("Day "+i+": Total Sales with Tax: "+withTax);
      }

      sum = 0;
    }
  }
}



//task4
import java.util.Scanner;

public class task4{
  public static void main (String [] agrs){
  
    Scanner Sc1 = new Scanner(System.in);
    Scanner Sc2 = new Scanner(System.in);
    Scanner Sc3 = new Scanner(System.in);
    
    System.out.print("Number of Members: ");
    int x = Sc1.nextInt();
    
    double rawSum = 0;
    
    for(int i = 1; i<=x; i+=1){
      System.out.print("Exercises for Member-"+i+": ");
      int y = Sc2.nextInt();
      

      for(int j = 1; j<=3; j+=1){
        System.out.print("Exercise-"+j+": ");
        double z = Sc3.nextInt();
        if(z>350){
          z=(z*0.5)+z;
        }
        rawSum = rawSum+z;
      }
        double avg = rawSum/3;
      if(y>3){
        System.out.println("(Can't do more than 3 exercise)");
      }
        if(avg>400){
          double total = (50*3+rawSum)/3;
          System.out.println("Average calories earned per day for Member-"+i+": "+total);
        }
        if(avg<200){
          double total = avg-avg*0.1;
          System.out.println("Average calories earned per day for Member-"+i+": "+total);
        }
      
      rawSum = 0;
    }
  }
}
```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass4.pdf">Tracing</a></H4>



<H2><u>Assignment - 5</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2005-%20Pattern%20Generation.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task 1
import java.util.Scanner;

public class ques1{
  public static void main(String [] args){
   Scanner sc = new Scanner(System.in);
   int n = sc.nextInt();
   
   
   for (int i = 1; i <= n; i++){
     for (int j = 1; j <= n - i; j++){
       System.out.print(" ");
     }
     for (int j = 1; j <= (2 * i - 1); j++){
       System.out.print(j);
     }
     System.out.println();
   }
        
   for (int i = n - 1; i >= 1; i--){
     for (int j = 1; j <= n - i; j++){
       System.out.print(" ");
     }
     for (int j = 1; j <= (2 * i - 1); j++){
       System.out.print(j);
     }
            System.out.println();
  }
  }
}


//task 2
import java.util.Scanner;

public class ques2{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = 1; i <= n; i++){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= i; j++){
        if (i == 1 || i == n || j == 1 || j == i){
          System.out.print(n - i + j);
        } else {
          System.out.print(" ");
        }
      }
      System.out.println();
    }
  }
}


//task 3
import java.util.Scanner;

public class ques3{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = 1; i <= n; i++){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= (2 * i - 1); j++){
        if (i == 1 || i == n || j == 1 || j == (2 * i - 1)){
          System.out.print(j);
        } else {
          System.out.print(" ");
        }
      }
      System.out.println();
    }
 }
}


//task 4
import java.util.Scanner;

public class ques4{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = 1; i <= n; i++){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= (2 * i - 1); j++){
        if (j == 1 || j == (2 * i - 1)){
          System.out.print(j);
        } else {
          System.out.print(" ");
        }
      }
      System.out.println();
    }
    
    for (int i = n - 1; i >= 1; i--){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= (2 * i - 1); j++){
        if (j == 1 || j == (2 * i - 1)) {
          System.out.print(j);
        } else {
          System.out.print(" ");
        }
      }
      System.out.println();
    }
  }
}


//task 5
import java.util.Scanner;

public class ques5{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = 1; i <= n; i++){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= i; j++){
        System.out.print(j);
      }
      for (int j = i - 1; j >= 1; j--){
        System.out.print(j);
      }
      System.out.println();
    }
  }
}


//task 6
import java.util.Scanner;

public class ques6{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = n; i >= 1; i--){
      for (int j = 1; j <= n - i; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= i; j++){
        System.out.print(j);
      }
      for (int j = i - 1; j >= 1; j--){
        System.out.print(j);
      }
      System.out.println();
    }
  }
}


//task 7
import java.util.Scanner;

public class ques7{
  public static void main(String [] args){
    Scanner sc = new Scanner(System.in);
    int n = sc.nextInt();
    
    for (int i = n; i >= 1; i -= 2){
      for (int j = 1; j <= (n - i) / 2; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= i; j++){
        System.out.print(j);
      }
      System.out.println();
    }
    
    for (int i = 3; i <= n; i += 2){
      for (int j = 1; j <= (n - i) / 2; j++){
        System.out.print(" ");
      }
      for (int j = 1; j <= i; j++){
        System.out.print(j);
      }
      System.out.println();
    }
  }
}

```
<H4>[No Tracing :>]</H4>



<H2><u>Assignment - 6</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2006-%20String.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
I lost my codes :<
```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass6.pdf">Tracing</a></H4>



<H2><u>Assignment - 7</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2007-%20Arrays.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task 1
import java.util.Scanner;

public class q1{
    public static void main (String[]agrs){
        Scanner Sc1 = new Scanner(System.in);

        System.out.print("N = ");
        int x = Sc1.nextInt();

        int [] arr1 = new int[x];

        for(int i = 0; i<x; i++){
            int num = Sc1.nextInt();
            arr1 [i] = num;
        }
        System.out.println("Original array:");
        for(int i = 0; i<x; i++){
            System.out.print(arr1[i] + " ");
        }

        System.out.println();
        
        System.out.println("After modifying:");
        for(int i = 0; i<x; i++){
            if(arr1[i]>=0){
                System.out.print(1 + " ");
            }
            else{
                System.out.print(0 + " ");
            }
        }
    }
}

//task 2
import java.util.Scanner;

public class q2{
    public static void main (String[]agrs){
        Scanner Sc1 = new Scanner(System.in);
        
        System.out.print("N = ");
        int N = Sc1.nextInt();
        int [] arr1 = new int[N];

        for(int i = 0; i<N; i++){
            System.out.print("Enter a number: ");
            int num = Sc1.nextInt();
            arr1[i] = num;
        }

        int x = Sc1.nextInt();
        boolean found = true;

        for(int i = 0; i<N; i++){
            if(arr1[i]==x){
                System.out.print(x + " is at index " + i);
                found = false;
                break;
            }
        }
        if(found == true){
            System.out.print("Element not found");
        }
    }
}

//task 3
import java.util.Scanner;

public class q3{
    public static void main (String[]agrs){
        Scanner Sc1 = new Scanner(System.in);
        Scanner Sc2 = new Scanner(System.in);
        
        System.out.print("Enter the length of the array: ");
        int length = Sc1.nextInt();

        double [] arr1 = new double[length];
        double sum = 0;

        for(int i = 0; i<length; i++){
            System.out.print("Enter a number: ");
            double num = Sc2.nextDouble();

            arr1[i] = num;
            sum = sum + num;
        }

        double max = 0;
        double min = 0;
        int maxpos = 0;
        int minpos = 0;
        for(int i = 0; i<length; i++){
            if(arr1[i]>=max){
                max = arr1[i];
                maxpos = i;
            }
            else if(arr1[i]<=min){
                min = arr1[i];
                minpos = i;
            }
        }
        System.out.println("Maximum element " + max + " found at index " + maxpos);
        System.out.println("Minimum element " + min + " founf at index " + minpos);
        System.out.println("Summation: " + sum);
        System.out.println("Average: " + sum/length);
    }
}

//task 4
import java.util.Scanner;

public class q4{
    public static void main (String[]agrs){
        Scanner Sc1 = new Scanner(System.in);


        System.out.print("Please enter the length of array 1: " );
        int length1 = Sc1.nextInt();
        
        int [] arr1 = new int[length1];
        System.out.println("Please enter the elements of arr1: ");

        for(int i = 0; i<length1; i++){
            int num1 = Sc1.nextInt();
            arr1[i] = num1;
        }


        System.out.print("Please enter the length of array 2: " );
        int length2 = Sc1.nextInt();
        
        int [] arr2 = new int[length2];
        System.out.println("Please enter the elements of arr2: ");

        for(int i = 0; i<length2; i++){
            int num2 = Sc1.nextInt();
            arr2[i] = num2;
        }

        boolean isSubset = true;
        for(int j = 0; j<length2; j++){
            boolean found = false;
            for(int i = 0; i<length1; i++){
                if(arr2[j] == arr1[i]){
                    found = true;
                    break;
                }
            }
            if(found == false){
                isSubset = false;
                break;
            }
        }

        if(isSubset == true){
            System.out.println("Array 2 is a subset of Array 1.");
        }
        else{
            System.out.print("Array 2 is not a subset of Array 1.");
        }
    }
}

//task 5
import java.util.Scanner;

public class q5 {
    public static void main(String[] args) {
        Scanner Sc1 = new Scanner(System.in);
        Scanner Sc2 = new Scanner(System.in);

        int[] marks = new int[5];
        System.out.println("Please enter the marks:");
        for (int i = 0; i < 5; i++) {
            int num = Sc1.nextInt();
            marks[i] = num;
        }

        String[] names = new String[5];
        System.out.println("Please enter the names:");
        for (int i = 0; i < 5; i++) {
            String text = Sc2.nextLine();
            names[i] = text;
        }


        for (int i = 0; i < marks.length - 1; i++) {
            for (int j = 0; j < marks.length - 1 - i; j++) {
                if (marks[j] > marks[j + 1]) {

                    int tempMark = marks[j];
                    marks[j] = marks[j + 1];
                    marks[j + 1] = tempMark;


                    String tempName = names[j];
                    names[j] = names[j + 1];
                    names[j + 1] = tempName;
                }
            }
        }

        System.out.println("Sorted Array:");
        for (int i = 0; i < marks.length; i++) {
            System.out.print(marks[i] + " ");
        }
        System.out.println();
        for (int i = 0; i < names.length; i++) {
            System.out.print(names[i] + " ");
        }
        System.out.println();
    }
}
```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass7.pdf">Tracing</a></H4>



<H2><u>Assignment - 8</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2008-%20Method.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task 1A
import java.util.Scanner;

public class q1a{
    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner(System.in);
        int x = Sc1.nextInt();

        boolean check = isPrime(x);
        System.out.println(check);
    }

    public static boolean isPrime (int x){
        if(x <= 1){
            return false;
        }
        for(int i = 2; i < x; i++){
            if(x%i == 0){
                return false;
            }
        }
        return true;
    }
}



//task 1B
import java.util.Scanner;

public class q1b{
    public static boolean isPerfect(int x){
        if(x<=0){
            return false;
        }
        int sum = 0;
        for(int i = 1; i < x; i++){
            if(x % i == 0){
                sum = sum + i; //0+1=1, 1+2=3, 3+3=6
                if(sum == x){
                    return true;
                }
            }
        }
        return false;
    }

    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner (System.in);

        int x = Sc1.nextInt();

        boolean check = isPerfect(x);
        System.out.println(check);
    }
}



//task 1C
import java.util.Scanner;

public class q1c{
    public static int isPerfect (int x){
        if(x<=0){
            return 0;
        }
        int sum = 0;
        for(int i = 1; i < x; i++){
            if(x % i == 0){
                sum = sum + i; 
                if(sum == x){
                    return x;
                }
            }
        }
        return 0;
    }

    public static int isPrime (int x){
        if(x <= 1){
            return 0;
        }
        for(int i = 2; i < x; i++){
            if(x%i == 0){
                return 0;
            }
        }
        return x;
    }

    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner (System.in);

        int x = Sc1.nextInt();

        int perfectNum = 0;
        int primeNum = 0;
        
        for(int i = 1; i <= x; i++){
            perfectNum = isPerfect(i) + perfectNum;
            primeNum = isPrime(i) + primeNum;

            int result = perfectNum + primeNum;
            if(i == x){
                System.out.println(result);
                break;
            }
        }
    }
}



//task 2A
import java.util.Scanner;

public class q2a{
    public static void showDots (int x){
        for(int i = 1; i <=x; i++){
            System.out.print(".");
        }
    }

    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner(System.in);

        int x = Sc1.nextInt();
        
        showDots(x);
    }
}



//task 2B
import java.util.Scanner;

public class q2b{
    public static void show_palindrome (int x){
        for(int i = 1; i <=x; i++){
            System.out.print(i);
        }

        for(int i = x-1; i > 0; i--){
            System.out.print(i);
        }
    }

    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner(System.in);

        int x = Sc1.nextInt();
        
        show_palindrome(x);
    }
}



//task 2C
import java.util.Scanner;

public class q2c {

    public static void showDots (int x) {
        for(int i = 1; i <= x; i++){
            System.out.print(".");
        }
    }

    public static void show_Palindrome (int x) {
        for(int i = 1; i <= x; i++){
            System.out.print(i);
        }

        for(int i = x - 1; i >= 1; i--){
            System.out.print(i);
        }
    }

    public static void showDiamond (int x) {
        for (int i = 1; i <= x; i++) {
            showDots(x - i);   
            show_Palindrome(i);  
            showDots(x - i);  
            System.out.println();
        }

        for (int i = x - 1; i >= 1; i--) {
            showDots(x - i);     
            show_Palindrome(i);    
            showDots(x - i);    
            System.out.println();
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int x = sc.nextInt();
        showDiamond(x);
    }
}



//task 3A
import java.util.Scanner;

public class q3a{

    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner (System.in);
        Scanner Sc2 = new Scanner (System.in);

        int x = Sc1.nextInt();
        int y = Sc2.nextInt();
        double t = calcTax(x, y);
        System.out.println(t);
    }

    public static double calcTax (int age, int tax){
        if (age < 18){
            return 0.0;
        }
        else if (tax < 10000){
            return 0.0;
        }
        else if (tax >= 10000 && tax <= 20000){
            return (0.07 * tax);
        }
        else if (tax > 20000){
            return (0.14 * tax);
        }
        else{
            return 0.0;
        }
    }
}



//task 3B
import java.util.Scanner;

public class q3b{
     public static void main (String [] agrs){
        calcYearlyTax ();
    }

    public static void calcYearlyTax (){
        Scanner Sc1 = new Scanner (System.in);
        Scanner Sc2 = new Scanner (System.in);

        int x = Sc1.nextInt();
        //int y = Sc2.nextInt();
        int y = 0;
        
        double [] arr = new double [12];
        for(int i = 0; i <= 11; i++){
        y = Sc2.nextInt();
        double t = calcTax(x, y);
        arr [i] = t;
        }

        for(int i = 0; i <= 11; i++){
        System.out.println("Month" + (i+1) + " tax: " + arr[i]);
        }
    }

    public static double calcTax (int age, int tax){
        if (age < 18){
            return 0.0;
        }
        else if (tax < 10000){
            return 0.0;
        }
        else if (tax >= 10000 && tax <= 20000){
            return (0.07 * tax);
        }
        else if (tax > 20000){
            return (0.14 * tax);
        }
        else{
            return 0.0;
        }
    }
}

```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass8.pdf">Tracing</a></H4>



<H2><u>Assignment - 9</u></H2>
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/Assignment%2009-%20Recursive%20Method.pdf">Questions</a>
  <H4>Solutions</H4>
  
```
//task 1
import java.util.Scanner;

public class task1{
    public static void main (String [] agrs){
        Scanner Sc = new Scanner (System.in);
        int n = Sc.nextInt();

        int x = factorial(n);
        System.out.println(x);
    }

    public static int factorial (int n){
        if(n > 0){
            return n*factorial (n-1);
        }
        else{
            return 1;
        }
    }
}



//task 2
import java.util.Scanner;

public class task2{
    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner (System.in);
        Scanner Sc2 = new Scanner (System.in);
        
        int base = Sc1.nextInt();
        int exponent = Sc2.nextInt();

        int x = power(base, exponent);
        System.out.println(x);
    }

    public static int power(int base, int exponent){
        if(exponent == 0){
            return 1;
        }
        else{
            return base*power(base, exponent-1);
        }
    }

}




//task 3
import java.util.Scanner;

public class task3{
    public static void main (String [] agrs){
        Scanner Sc1 = new Scanner (System.in);
        Scanner Sc2 = new Scanner (System.in);

        System.out.print("Length of array: ");
        int L = Sc1.nextInt();

        int [] arr = new int [L];
        for(int i = 0; i < L; i++){
            System.out.print("Enter array value: ");
            int x = Sc1.nextInt();
            arr [i] = x;
        }

        System.out.print("Index: ");
        int index = Sc2.nextInt();

        printElement(arr, index);
    }

    public static void printElement(int [] arr, int index){
        if(index < arr.length){
            System.out.println(arr[index]);
            printElement(arr, index+1);
        }
        
    }

}




//task 4
import java.util.Scanner;

public class task4{
    public static void main (String [] agrs){
        Scanner Sc = new Scanner (System.in);
        int x = Sc.nextInt();

        if(x >= 0){
            System.out.println(fibonacci(x));
        }
    }

    public static int fibonacci(int n){
        if(n == 0){
            return n;
        }
        else if(n == 1){
            return n;
        }
        else{
            return fibonacci(n-1)+fibonacci(n-2);
        }
    }

}
```
<H4><a href ="https://github.com/RSK48/BracU-CSE110-2026/blob/main/ass9.pdf">Tracing</a></H4>



