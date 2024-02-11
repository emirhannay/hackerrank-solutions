We define the following terms:

Lexicographical Order, also known as alphabetic or dictionary order, orders characters as follows:
For example, ball < cat, dog < dorm, Happy < happy, Zoo < ball.

A substring of a string is a contiguous block of characters in the string. For example, the substrings of abc are a, b, c, ab, bc, and abc.
Given a string, , and an integer, , complete the function so that it finds the lexicographically smallest and largest substrings of length .

Function Description

Complete the getSmallestAndLargest function in the editor below.

getSmallestAndLargest has the following parameters:

string s: a string
int k: the length of the substrings to find
Returns

string: the string ' + "\n" + ' where and are the two substrings
Input Format

The first line contains a string denoting .
The second line contains an integer denoting .

Constraints

consists of English alphabetic letters only (i.e., [a-zA-Z]).

Sample Input : welcometojava
3

Sample Output :
ava
wel


```java
public static String getSmallestAndLargest(String s, int k) {   

    String smallest = "";
    String largest = ""; 
    //The reason i write s.length()-k+1 for the length of the array is that it is ordered combination length
    String list[] = new String[s.length()-k+1];

    for(int i=0; i < s.length()-k+1 ; i++) {

        String temp = s.substring(i,i+k); 
        list[i] = temp;
    }
    
        //sort alphabetically
    java.util.Arrays.sort(list);

    System.out.println(list[0]);
    System.out.println(list[list.length-1]);

    return smallest + "\n" + largest;
}
```