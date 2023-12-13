# backend-code-challenge

Welcome to the coding challenge! We're glad you made it so far! :)

# What are we building?

In this coding challenge we'll be building a very simple API for a social network app. Think
of it as an overly simplified version of Instagram.

Three domain objects will be used: `User`, `Post` and `Like`. These domain objects represent
concepts we all know and use in a way or another. These classes are already created in the project.

```java

/**
 * A User represents a user account in our fake Instagram example.
 *
 * A User must have:
 *
 * - a username.
 * - a set of {@link Post}.
 * - a creation timestamp.
 * - a country code.
 * - a phone number.
 */
public class User {

}
```

```java

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

This project was generated with Spring initializr and it has these dependencies:

- H2 Database
- Lombok
- Spring Data JPA
- Spring Web
- Spring Boot DevTools

# What should be implemented?

- The domain objects shown above should be converted to JPA entities, and their fields should be created and
  mapped to columns following the instructions in their corresponding JavaDocs. Remember that H2 is set up 
  as an in memory database, so you don't need to add an external dependency if you don't want to, if you feel
  more comfortable adding Postgres/MySQL feel free to do that. Make sure the IDs are generated as an integer number.
  
- Now that the domain objects are mapped to the database as JPA entities, repositories and services should be 
  created that will allow us to make CRUD operations. In this case we'll only create the service and repository
  for `User` domain object
  
- The next step is to create a controller that will allow us to do the following:
  
    - Create a `User`. Check that the username is unique and if it's not unique handle the exception with an `@ExceptionHandler`.
  
    - Update a `User`. Remember that usernames must be unique and exceptions should be handled.

    - Get all the `User`s. In the response only the username should be included and not all the posts the user has.
      
    - Get a user
     
    - Delete a single user

    - Delete multiple users
  
    - The comments are handled by another service. Create an endpoint and a client that consumes this 
      API https://jsonplaceholder.typicode.com/ to get the comments related with a specific post.
  
    - Create an endpoint that recovers the phone code and currency for User by calling this SOAP web
      service http://webservices.oorsprong.org/websamples.countryinfo/CountryInfoService.wso?WSDL. 
      You can find more information about this service here: https://documenter.getpostman.com/view/8854915/Szf26WHn#33a2b225-11a6-48d3-a695-fb0989cc4971
  
# What do I need to do for brownie points?
  
- In order to see that everything works it would be nice to create a `@SpringBootTest` to test the integration between all 
  the application layers.
  
- It would also be nice to have a mechanism that logs the user-agent in the console on each HTTP request that is made.

# How do I start?

Remember that you can use Lombok since it has been added as a dependency.

In order to start coding please fork this repository and commit the changes under your username in your own repo. When finished
add peter-catalin as a collaborator to that repo. :)

Happy coding!
