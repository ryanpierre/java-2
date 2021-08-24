# Demo notes

- Getters and setters - where did my attr_reader, attr_writer, and attr_accessor go ?
- Constructors ?
- Standard Exceptions vs Custom Exceptions
  - Demonstrate using the ArithmeticError as well as a BankAccountError
  - https://www.geeksforgeeks.org/types-of-exception-in-java-with-examples/
- Making our own custom exception BankAccountError
    ```java
    public class BankAccountException extends Exception {
        private Integer secretCode;

    	public BankAccountException(String message, Throwable cause, Integer secretCode) {
    		super(message, cause);
    		this.secretCode = secretCode;
    	}

        public BankAccountException(String message, Throwable cause) {
    		super(message, cause);
    	}

        public Integer getSecretCode() {
            return this.secretCode;
        }
    }
    ```

- Walk through a TDD approach of Testing exceptions by implementing the withdraw function
  - Demo a beforeEach and a beforeAll because it starts out to get tedious to keep instantiating the class
    ```java
    private BankAccount subject;

      @BeforeEach
      void setup() {
          System.out.println("New test started.");
          subject = new BankAccount();
      }

      @AfterEach
      void teardown() {
          System.out.println("Test ended.");
      }
    ```
  - https://howtodoinjava.com/junit5/expected-exception-example/
