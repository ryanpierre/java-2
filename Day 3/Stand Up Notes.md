# Stand Up

- Assert Instance Of 
  - Why would I want to assert something is an instance of something else ?
  - What should I actually be testing ?

- BDD (variant of TDD)
- Behaviour Driven Development 
- Rspec <-- BDD Library
- Jest <-- BDD Library
- Junit <-- can be BDD (it should be)
- Test behaviours not implementations.

- attr_reader, attr_accessor, attr_writers

```ruby
    require 'bcrypt'
    class MyClass 
        attr_accessor :id

        def id
            @id
        end

        def id(newId)
            @id = newId
        end
    end
```


```java

    public class MyClass {
        private int id = 0;

        public getId() {
            return this.id;
        }

        public setId(int newId){
            this.id = newId;
        }

        public catCounter(int numCats) {
            this.id += numCats;
        }
    }

    MyClass example = new MyClass();
    example.catCounter(5)
        assertEquals(5, example.getId())
```

```javascript
    // sort this list of letters alphabetically

    myarray.filter((item) => item instanceof String).sort((a, b) => b - a)
```




