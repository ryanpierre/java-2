"Hi, is there any files relating to gradle or any other we should put in .gitignore or just git add everything?"

Use the official Gradle docs: https://github.com/gradle/gradle/blob/master/.gitignore

"Why do I have to import some classes but not others like String or my test subject class?"

- Everything in the java.lang package is automatically imported into any java file. Since ArrayList is in java.util we still have to import it to use it
- Everything in the package you're currently in is also automatically imported. Which is why we don't import FizzBuzz into FizzBuzzTest. (i.e. if you made your GroupId com.ryanpierre, everything in com.ryanpierre is also automatically imported)

"Which GroupId should we use when setting up tryout in IntelliJ?"

You can use whatever you like ! com.yourname , org.spacel0rd , art.artman . It's most common to use your own personal website or the company you work for but it doesn't really matter for these projects."