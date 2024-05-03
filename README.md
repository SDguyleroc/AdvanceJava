# AdvanceJava

## Introductions to generics in Java

## For Loops
### Loop that executes a specified number of times
#### Its is count controlled as opposed to condition controlled. count control means the "For loop" executes a specified number of times.

### Problem

#### Write a cashier program that will scan a given number of items and tally the cost.

import java.util.Scanner;

public class Chashier {

    public static void main(String[] args) {
        
        //Get number of items to scan 

        System.out.print("Enter the number of items you would like to scan: ");

        Scanner scanner = new Scanner(System.in);
         int quantity = scanner.nextInt();

        double total = 0;

        // Create loop to iterate through all of the items and accumulate the costs

        for(int i =1; i<=quantity; i++){

            //System.out.print("Enter the cost of the item 1 : ");
                 
            System.out.print("Enter the cost of the item " + i + " : ");
           
            double price = scanner.nextDouble();

            total =total + price;


        }

        scanner.close();
        System.out.println("Your total is: " + total);

    }

}

### For loop are Count Controlled
##### Loop runs a specified number of times.

### Pretest
##### Condition is tested before entering the lopp.

### Execution
##### Best to use when you know howmany time the loop should be executed.

## Nested Loops

Loopes Inside of loops

## Problem
### Find the average test score for each student in the class. There are 24 students and four tests.

import java.util.Scanner;

public class AverageTestScores {

    public static void main(String[] args) {
        
        // Initialize what we know

        int numverOfStudent = 24;
        int numberOfTests = 4;

        Scanner scanner = new Scanner(System.in);

        // let's proccess all students
        for(int i=0; i<numverOfStudent; i++){

            double total= 0;

            System.out.println("___________Student: " + (i+1)+ "___________");

            //process a student's test scores

            for(int j=0; j<numberOfTests;j++){

                System.out.println("Enter the score for test #" + (j+1) + " : ");

                double score = scanner.nextDouble();

                total= total + score;

            }

            double average = total/numberOfTests;
            System.out.println("The test avarage for student #" + (i+1) + " is: " + average);
        }




        scanner.close();
    }

}
















