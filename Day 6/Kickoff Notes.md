# Kickoff 2

- Initialize with spring boot using spring initialzr 
  - Spring Web
  - H2 Database 
  - Spring JPA
- Why not just write SQL rather than using an ORM such as User.find ? 
  - Security
  - Optimized
- Model View Controller (MVC) pattern
  - Domain Modelling 


What do we remember about MVC / Sinatra/ Rails ?
- Model is where you store your classes, View is where you render templates, Controller links them up and runs some logic or tells the model to run some logic
- Separation of concerns
- SRP taken to the next level
- Controller sometimes contains routes (more on this ...)


Model
- "Model" our database ! We often refer to these as entities, and the process of deciding what our models should be, how they're validated and how they relate to the database is called entity mapping. 

Noun / Verb , UML diagrams

DAO
- DAO (Data access objects) the DAO, Model, and Database all work together to ensure that my App doesn't need to know exactly how my database is set up. 

- Model <> Database, My model needs to know exactly how my database is set up 
- Model <> DAO <> Database 

@Entity
public class User {

}

public interface DAO<T> {
    get (long id)

    List<T> getAll() 

    void save(T t);

    void update(T t, String[] params)

    void delete(T t);
}

- Domain Modelling 101 review
  - How do we start a project ? Where do we begin ?
  - @Entity
- Inversion of Control
  - @Autowired
- Dependency Injection 
  - DI Container

  @Autowired
  CatService cs;

- Talk about outline for the week
  - 4 days
  - Twitter Seed - stories