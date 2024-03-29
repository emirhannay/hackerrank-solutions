The username consists of 8 to 30 characters inclusive. If the username consists of less than 8 or greater than 30 characters, then it is an invalid username.
The username can only contain alphanumeric characters and underscores (_). Alphanumeric characters describe the character set consisting of lowercase characters [a-z] , uppercase characters [A-Z] , and digits [0-9].
The first character of the username must be an alphabetic character, i.e., either lowercase character [a-z]  or uppercase character [A-Z] .

```java
public static final String regularExpression = "^[a-zA-Z][a-zA-Z0-9_]{7,29}$";
```

```
^ : Indicates the start of the pattern.
[a-zA-Z] : Ensures that the first character is a letter (either uppercase or lowercase).
[a-zA-Z0-9_] : Includes alphanumeric characters and underscore.
{7,29} : Specifies that the length should be at least 8 and at most 30 characters.
$ : Indicates the end of the pattern.
```