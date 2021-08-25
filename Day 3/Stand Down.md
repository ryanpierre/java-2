# Stand Down !

Did anything feel like it made more sense today ?

- Constructors 
- "Less painful in general" to paraphrase (in quotes)
- More comfortable with what to search for when seeking help
- Yesterday: "General Syntax - I'm never going to understand this" Today: "Ok this kind of makes sense" 

Did anything feel like it made less sense ?
- Errors - so many types ! <--- 
- Static keyword: Class Method ? Instance Method ?
  - Why is it removing it or adding it ? <---


```java
    public class MyClass {
        private String name = "Ryan";

        public static String myStaticMethod() {
            return this.name.toLowerCase()
        }

        public String getName() {
            return this.name;
        }
    }
```


```java
    public class MyClass {
        private String name;

        public void MyClass(String initialName) {
            
        }

        public void setName(String newName) {
            this.name = newName;
        }

        public String getName() {
            return this.name;
        }
    }
```
Anything new we encountered that was difficult ?
- Motivation 
- Sort an ArrayList
  - Lists ? ArrayLists ? Collections ? 
- Dependency Injection
  - Mocking ?
- Any benefit to key value pairs in java
  - HashMap ?


DATATYPES <--- in our demo ArrayList, List, HashMap, whatever else
MOCKING <---  