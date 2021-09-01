# Stand Down

- What was your favourite part of java so far ?
  - Explicitness 
  - Being good at java = being coding wizard
  - IntelliJ
  - Multiple methods same name / different calls
  - Constructors 


- What was hard today ? Or this weekend ... (for those who did the REST service :p)
  - Every. little. Thing.  Had to ask for help on every step which with disheartening
    - Ended up adding column thru table plus   
  - Trying to figure out how to add a column to the db
  - Setting up test database 
  - Test the db, set up the testing database
  - Database migrations like rails ? 

How to add a dependency (and maybe when ?)
How to make a migration ? 
Controllers ? 

We're gonna build one (1) feature together E2E
    - Adding a column
    - Migration if possible
    - A new route in a controller and interacting with the database
    - What is the purpose of toString()?


```java
public class Anything {
    private Integer id;
    private String name;

    Anything(Integer id, String name) {
        this.id = id;
        this.name = name;
    }

    @Override
    public boolean equals(Anything anything) {
       return this.id == anything.id && this.name == anything.name;
    }

    @Override
    public String toString() {
        return id.toString();
    }
}

Anything anything = new Anything(2, "ryan");
Anything anything2 = new Anything(2, "ryan");

anything.equals(anything2) //true

System.out.println(anything);

"This anything has an id 2 and a name ryan";



