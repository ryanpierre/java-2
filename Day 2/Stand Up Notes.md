# Stand Up / Demo

## Rapid fire questions 

### Is there a null type in Java ?

The answer is YES ! `null` 

`void` return type, this truly means it returns NOTHING

`null` != Nothing 

`null` IS A VALUE 

`null` in JavaScript, it will be the exact same in Java

if you're used to `nil` in ruby, it will be the exact same in Java

TypeScript is a HUGE exception to this. but normally, compiled languages don't have a concept of undefined. 

NullPointerException 

```javascript
var thing;

console.log(thing); //undefined
```

```java
private int cat;

System.out.printLn(cat) //NullPointerException
```

### Console log ? 

#### Memorize this
System.out.printLn("Hello")


#### Memorize this
public static void main(String[] args) {

}

### int vs Integer 

String and char[]

char myChar = "a"; <--- single string character
char[] myCharArray = ["a", "b", "c"]

String ~= myCharArray

WRAPPER CLASS

String and Integer are CLASSES

"hello".downcase 
"hello".upcase 

5.toString()

private int myNumber = 5;

myNumber.toString() // ERROR 

private Integer myNumber2 = 5;

myNumber2.toString() // OK !

myNumber == myNumber2

String is a wrapper for char[]
Integer is a wrapper for int

## Demo - getting visibility, debugging, using intelliJ well 