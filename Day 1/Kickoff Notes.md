# Java Kickoff

## What do we know about Java ????????????????????

- Quite a dated language 
- Object Oriented: JavaScript ... you don't have a choice !!!!!! you have to do it object oriented
- you have to be specific about data types (is it an int ? is it a String ? ) "statically typed"
- Compiled !!!
- Heavily used in back end development
- it's an island !?
- Uncle bob's lecture examples in java

Java, **is a statically typed compiled language.**

## Compiled vs interepreted languages ?

- Browser interpreting javascript and displaying the code
- Compiled langauge cannot****** be changed in real time (there technically is tooling available to do this, but it's not a feature of the language)

- compiled languages process of compilation first. 

.java -> Bytecode -> something really basic the machine understands ... sometimes we call this Machine Code 
.kotlin -> Bytecode -> something really basic 

## JRE, JDK, JVM

- Java Runtime Environment -  Installing Java 11 Runtime, Java 8 Runtime, allows us to run java apploications. This will be specific to mac, windows, linux
- Java Development Kit - a set of tools and libraries required to develop Java DEVELOPING JAVA. This will be specific to mac, windows, linux
- Java Virtual Machine <----- Scala, Groovy, Kotlin <-- also pretty helpful. Runs the bytecode ! This is agnostic to windows, mac, or linux = Portability !!

# statically typed ??? 
- C 
- Java
- TypeScript 

What types are my variables ? What types are my arguments ? and what types (if any) are my return values ? 

def my_method(arg1) 
    arg1.downcase
end

my_method(2)

// 2 is an integer, and it doesn't have the downcase ... ERROR

def my_method(arg1: String) 
    arg1.downcase
end

my_method(2)

// Error BEFORE WE EVEN RUN THE CODE - COMPILER ERROR 

Runtime Errors - python ruby js etc\
Compiler Errors - errors that happen before we even run our code ...

# Why might compiler errors be useful (and maybe even great ?)

- More efficient process - catch an error before we start eating memory 🍔
- We have visibility into what functions are actually doing ! 
- Allows for greater planning and efficiency when writing code 

# IDE 
- VSCode , Atom, Sublime 
- IntelliJ IDEA Community Edition <---- IntelliJ

## Gradle, Maven, etc

Dependency managers, metadata managers and task runners.

**What do we know about a Gemfile?**
- Dependency management, declare whatever is needed to run your program
- When working with someone else 

**What is the structure of a package.json ?**
Package.json
{
    scripts: {
        dev: "gdgsdg"
        start: "node index.js",
        test: "sgagd"
    }
    engine: "node 10",
    author: "ryan"
}

**How do we run a ruby app ?**
ruby app.rb

**js ?**
yarn start

## Package Names

mypackage.mywebsite.com = com.mywebsite.mypackage in java

org.example.HelloWorld
com.java.util.lang

lang.util.java.com
helloworld.example.org


