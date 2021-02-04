# backend-code-challenge

Welcome to the coding challenge! We're glad you made it so far! :)

#What are we building?

In this coding challenge we'll be building a very simple API for social network app. Think
of it as an overly simplified version of Instagram.

Three domain objects will be used: `User`, `Post` and `Like`. These domain objects represent
concepts we all know and use in a way or another. These classes are already created in the project.

```java
package com.lendismart.backendinterview.domain;

/**
 * A User represents a user account in our fake Instagram example.
 *
 * A User must have:
 *
 * - a username.
 * - a set of {@link Post}
 * - a creation timestamp.
 */
public class User {

}
```

```java
package com.lendismart.backendinterview.domain;

/**
 * A Post is something a user uploads, therefore it belongs to a user.
 *
 * A Post must have:
 *  - a URL that points to an image.
 *  - a set of {@link Like}.
 *  - a creation timestamp.
 */
public class Post {

}
```

```java
package com.lendismart.backendinterview.domain;

/**
 * A Like belongs to a {@link Post}
 *
 * A Like must have
 *  - a {@link User} indicating who gave the like
 *  - a creation timestamp.
 */
public class Like {

}
```

This project was generated with spring initializr and it has these dependencies:



# What should be implemented?

- The domain objects shown above should be converted to JPA entities, and their fields should be created and
  mapped to columns following the instructions in their corresponding JavaDocs. Remember that H2 is set up 
  as an in memory database, so you don't need to add an external dependency if you don't want to, if you feel
  more comfortable adding Postgres/MySQL feel free to do that.
  
- Now that the domain objects are mapped to the database as JPA entities, repositories and services should be 
  created that will allow us to make CRUD operations. Also, tests must be written to ensure that our mappings 
  are correct and objects can be persisted to the database.
  
- The next step is to create controllers that will allow us to do the following:
  
    - Create a `User`. Check that the username is unique and if it's not unique handle the exception with an `@ExceptionHandler`.
  
    - Change the username of `User`. Remember that usernames must be unique and exceptions should be handled.

    - Get all the `User`s. In the response only the username should be included and not all the posts the user has.
      
    - Create a `Post`.

    - Get all the posts belonging to a specific `User`. In the response, each `Post` should include the `Like`s it has.
  
    - Delete a single `Post`.
  
    - Delete multiple `Post`.

    - Create a `Like` for a specific post.
  
    - Delete a `Like`.
  
    - An endpoint that will return in a `List` the username and the number of likes he/she got in the last month.
  
# What do I need to do for brownie points?
  
- In order to see that everything works it would be nice to create a `@SpringBootTest` to test the integration between all 
  the application layers.
  
- It would also be nice to have a mechanism that logs the user-agent in the console on each HTTP request that is made.

- Add JavaDocs

- Decouple and make the code as reusable and generic as it makes sense to be.


Remember that you can use Lombok since it has been added as a dependency.

In order to start coding please fork this repository and commit the changes under your username in your own repo. When finished
add peter-catalin as a collaborator to that repo. :)

Happy coding!