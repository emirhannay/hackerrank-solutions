The elements of a String are called characters. The number of characters in a String is called the length, and it can be retrieved with the String.length() method.

Given two strings of lowercase English letters,  and , perform the following operations:

Sum the lengths of A and B.
Determine if A is lexicographically larger than B (i.e.: does B come before A in the dictionary?).
Capitalize the first letter in A and B and print them on a single line, separated by a space.

#### Input Format

The first line contains a string A. The second line contains another string B. The strings are comprised of only lowercase English letters.

#### Output Format

There are three lines of output:
For the first line, sum the lengths of A and B .
For the second line, write Yes if A is lexicographically greater than B otherwise print No instead.
For the third line, capitalize the first letter in both A and B and print them on a single line, separated by a space.

#### Sample Input 0
```
hello
java
```
#### Sample Output 0
```
9
No
Hello Java
```

#### Explanation 0

String A is "hello" and B is "java".

A has a length of 5 , and B has a length of 4 ; the sum of their lengths is 9 .
When sorted alphabetically/lexicographically, "hello" precedes "java"; therefore,A  is not greater than B and the answer is No.

When you capitalize the first letter of both A and B and then print them separated by a space, you get "Hello Java".

```java

        Scanner sc=new Scanner(System.in);
        String A=sc.next();
        String B=sc.next();
        System.out.println(A.length() + B.length());
        int result = A.compareTo(B);
        if ( result < 0){
            //If A greater than B
            System.out.println("No");
        }
        else if ( result > 0) {
            //If B greater than A
            System.out.println("Yes");
        }
        else {
            //If equals
            System.out.println("No");
        }
        String upperCaseStringA = Character.toUpperCase(A.charAt(0)) + A.substring(1);
        String upperCaseStringB = Character.toUpperCase(B.charAt(0)) + B.substring(1);
        
        System.out.println(upperCaseStringA + " "+ upperCaseStringB);

```
