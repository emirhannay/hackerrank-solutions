Two strings,  and , are called anagrams if they contain all the same characters in the same frequencies. For this challenge, the test is not case-sensitive. For example, the anagrams of CAT are CAT, ACT, tac, TCA, aTC, and CtA.

### Function Description

Complete the isAnagram function in the editor.

isAnagram has the following parameters:

string a: the first string
string b: the second string
Returns

boolean: If  and  are case-insensitive anagrams, return true. Otherwise, return false.
### Input Format

The first line contains a string .
The second line contains a string .

### Constraints

Strings  and  consist of English alphabetic characters.
The comparison should NOT be case sensitive.
### Sample Input 0
anagram
margana
### Sample Output 0
Anagrams

### Sample Input 1
anagramm
marganaa
### Sample Output 1
Not Anagrams


```java

static boolean isAnagram(String a, String b) {
       
       
    char[] tempa = new char[a.length()];
    char[] tempb = new char[b.length()];

    //Length control
    if (a.length() != b.length()) {
        return false;
    }

    //We are sending all the letters of the strings into array
    for (int i = 0; i < tempb.length; i++) {
        tempa[i] = a.toLowerCase().charAt(i);
        tempb[i] = b.toLowerCase().charAt(i);
    }
    //Then we are sorting them using the Arrays.sort method
    java.util.Arrays.sort(tempa);
    java.util.Arrays.sort(tempb);

    //If these two strings contain the same number of the same letters,
        // after sorting, they will result in arrays with identical values, where each index will hold the same character.
    for(int i=0;i<tempb.length;i++){
        if(tempa[i]!=tempb[i])
            return false;
    }
    return true;
}

```