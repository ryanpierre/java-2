"Why is my program not running when I throw an exception"

Nothing is catching that exception. Need to explain bubbling of exceptions.

```java

class Main {
    public static void main(String[] args) {
        BankAccount bankAccount = new BankAccount()

        try {
            bankAccount.deposit(-100)
        }

        catch(ArithmeticExpression e) {
            // Print the caught error
            System.out.println(e);
        }
    }
}
```