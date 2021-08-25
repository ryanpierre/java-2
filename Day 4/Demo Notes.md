# Demo

### Describe blocks 
- In Junit5 we use the annotations @Nested and @DisplayName to achieve more rspec like readability of our tests: https://junit.org/junit5/docs/current/user-guide/#writing-tests-nested
- Variables instantiated in the parent are accessible by children / nested classes
- We can apply before each and after each to each scope
- We can use DisplayName to make our tests more readable

```java
  @DisplayName("A stack")
  class TestingAStackDemo {

      Stack<Object> stack;

      @Test
      @DisplayName("is instantiated with new Stack()")
      void isInstantiatedWithNew() {
          new Stack<>();
      }

      @Nested
      @DisplayName("when new")
      class WhenNew {

          @BeforeEach
          void createNewStack() {
              stack = new Stack<>();
          }

          @Test
          @DisplayName("is empty")
          void isEmpty() {
              assertTrue(stack.isEmpty());
          }

          @Test
          @DisplayName("throws EmptyStackException when popped")
          void throwsExceptionWhenPopped() {
              assertThrows(EmptyStackException.class, stack::pop);
          }
      }
  }
```
  
### Mocking / DI
- Make a private class inside your test class
- Use an interface to enforce a contract between your mock and your real class
- IDiary convention

```java
    private class MockDiary implements IDiary {
        public Boolean iGotCalled = false;

        public String read() {
            // If you wanted to assert on what a method really got called with.
            // You could assign it to a field. We'll use this to be doubly
            // sure that `read` isn't called when `SecretDiary` is locked.
            iGotCalled = true;
            return "You've successfully called through to MockDiary";
        }
    }
```

Theme: A lot of classes everywhere !

### Data types
- HashMaps: We should only use these if we **don't know** what fields the object will have, if we **do** know we should opt for a class. It's more efficient both in terms of speed and memory. 
- 

### If we have time

Overrides
- Every Class is a subclass of Object in Java
- That means, sometimes we have built in functions to our classes we didn't even know we had ! 
- Remember .toString() ? And how I said that calling System.out.println() implicitly calls the .toString() method on whatever class is inside ? You can override any built in object function with your own if you'd like.
- This is pretty useful for things like equals and toString for example. You do this using the @Override annotation.


## Main Demo - Pizza

- Show the nested tests and test naming
- Create the PizzaPlace class which has an arraylist of Pizza
- ArrayList - basically what you would use an array for in every other language. implements List
- add, remove, removeIf, get
- HashMaps - for when you don't know what all the keys will be... perhaps remaining ingredients ? implements Map. Maybe creating a pizza makes you reduce the ingredient amounts ?
- Show how you can refactor that into a Topping class, use an array list of toppings, and use an enum for the topping type. Default 16, but grows automatically re: HashmapSize
- get(), put(), and remove()
- 