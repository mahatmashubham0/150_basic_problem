# Finding the Sum of Digits of a Number Until Zero
# Description: Write a program to repeatedly sum the digits of a number until the result is zero.
# Example:
# Input: number = 123
# Output: 6
# Explanation: Sum of digits is 1 + 2 + 3 = 6; sum of digits of 6 is 6 (which is a single digit).

class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Try programiz.pro");
        int n = 415 , rem , sum = 0;
        while(n > 0) {
            rem = n % 10;
            sum = sum + rem;
            n = n / 10;
        }
        
        System.out.println(sum);
    }
}

# Generating a Multiplication Table for a Range
# Difficulty: Easy
# Topics: Arrays, Basic Programming
# Description: Write a program to generate multiplication tables for numbers within a specified range.
# Example:
# Input: start = 2, end = 4
# Output: 2 x 1 = 2   3 x 1 = 3   4 x 1 = 4  
#         2 x 2 = 4   3 x 2 = 6   4 x 2 = 8  
#         2 x 3 = 6   3 x 3 = 9   4 x 3 = 12  
#         2 x 4 = 8   3 x 4 = 12  4 x 4 = 16 

class HelloWorld {
    public static void main(String[] args) {
        int start = 2 , end = 4;
        for(int i = 2 ; i <= 4 ; i++) {
            for(int j = 1 ; j <= 4 ; j++) {
                System.out.println(i + " * " + j + " = "+i*j);
            }
            System.out.println();
        }
    }
}

<!-- Calculating the Sum of a Series (1 + 1/2 + 1/3 + ... + 1/n)
Description: Write a program to calculate the sum of the series 1 + 1/2 + 1/3 + ... + 1/n up to the nth term.
Example:
Input: n = 4
Output: 2.083333
Explanation: Sum of the series is 1 + 1/2 + 1/3 + 1/4 ≈ 2.083333. -->

class HelloWorld {
    public static void main(String[] args) {
        // int n = 1 , 1/2 , 1/3 , 1/4;
        int n = 4;
        double sum = 0 , d;
        for(double i = 1 ; i <= n ; i++) {
            d = 1.0/i;
            sum = sum + d;
        }
        
        System.out.println(sum);
    }
}

<!-- Finding All Pairs of Elements in an Array that Add Up to a Given Sum
Description: Write a program to find all pairs of elements in an array whose sum equals a specified target.
Example:
Input: array = [1, 2, 3, 4, 5], target = 5
Output: [(1, 4), (2, 3)]
Explanation: Pairs that sum up to 5 are (1, 4) and (2, 3). -->

// Online Java Compiler
// Use this editor to write, compile and run your Java code online

class HelloWorld {
    public static void main(String[] args) {
        
        int count = 0, target = 5;
        int[] array = {1, 2, 3, 4, 5};
        for(int i = 0 ; i < array.length ; i++) {
            for(int j = i+1 ; j < array.length - 1 ; j++) {
                if(array[i] + array[j] == target) {
                    count++;
                    System.out.println(array[i] +" , "+ array[j]);
                }
            }
        }
        
        System.out.println(count);
    }
}

<!-- Generating a Diamond Pattern of Stars
Difficulty: Medium
Topics: Patterns, Basic Programming
Description: Write a program to create a diamond pattern with stars of a given size.
Example:
Input: size = 5
Output:
  *  
 ***  
*****  
 ***  
  *   -->

// Online Java Compiler
// Use this editor to write, compile and run your Java code online
//   *  
//  ***  
// *****  
//  ***  
//   *  
class HelloWorld {
    public static void main(String[] args) {
      
      int n = 3;
      //   upper bound
      for(int i = 1 ; i <= n ; i++) {
        for(int j = 1 ; j <= n-i ; j++) {
            System.out.print(" ");
        }
        for(int j = 1 ; j <= 2*i-1 ; j++) {
            System.out.print("*");
        }
        System.out.println();
      }
      
      // Lower bound
      for(int i = n-1 ; i >= 1 ; i--) {
         for(int j = 1 ; j <= n-i ; j++) {
             System.out.print(" ");
         }      
         for(int j = 1 ; j <= 2*i-1 ; j++) {
             System.out.print("*");
         }
            System.out.println();
      }
        
    }
}

<!-- Counting the Number of Palindromic Substrings in a String
Description: Write a program to count how many palindromic substrings exist in a given string.
Example:
Input: string = "aaa"
Output: 6
Explanation: Palindromic substrings are "a", "a", "a", "aa", "aa", "aaa". -->


<!-- 
Generating a Matrix with Multiplication Table
Description: Write a program to generate a matrix where each element at position (i, j) is the product of i and j.
Example:
Input: size = 3
Output: 
1 2 3  
2 4 6  
3 6 9  -->

class HelloWorld {
    public static void main(String[] args) {
      
      int n = 3;
      int arr[][] = new int[n][n];
      
      for(int i = 0 ; i < n ; i++) {
          for(int j = 0 ; j < n ; j++) {
              arr[i][j] = (i+1) * (j+1);
          }
      }
      
      for(int i = 0 ; i < n ; i++) {
          for(int j = 0 ; j < n ; j++) {
              System.out.print(arr[i][j]);
          }
          System.out.println();
      }
        
    }
}

<!-- Finding the GCD of Multiple Numbers
Description: Write a program to find the GCD (Greatest Common Divisor) of an array of numbers.
Example:
Input: array = [12, 24, 36]
Output: 12
Explanation: The GCD of 12, 24, and 36 is 12. -->



<!-- Finding the Sum of the First N Odd Numbers
Difficulty: Easy
Topics: Mathematical Computations
Description: Write a program to calculate the sum of the first N odd numbers.
Example:
Input: N = 5
Output: 25
Explanation: Sum of the first 5 odd numbers (1 + 3 + 5 + 7 + 9) is 25. -->

class HelloWorld {
    public static void main(String[] args) {
      
      int n = 5 , sum = 0 , cnt = 0;
      for(int i = 1 ; i <= 1000000000 ; i++) {
          if(i % 2 != 0) {
              sum += i;
              cnt++;
              System.out.println(sum);
          }
          if(cnt == n) {
              break;
          }
      }
      
      System.out.println(sum);
    }
}
