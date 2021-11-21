# graphQLmern
# 21 GraphQL-enabled MERN stack application

# REact MERN Homework

## Overview

In this homework, you will be finishing the completion of a GraphQL-enabled MERN stack application.

### Server-Side Work

In the server area, you need to do the following:

* In the _server/server.js_ file, instantiate the Apollo server. Make sure you also add in the authMiddleware, which has already been required in  for you.

* In the _server/schemas/typeDefs.js_ file:
    * Add a data type for Book. It should support fields for bookId (ID datatype), authors(String), description(String), link(String), and title(String). The bookId and the title should be required.
    * Add a Mutation entry for login. It should accept email and password parameters, both required Strings, and should point to the Auth data type.

* In the _server/schemas/resolvers.js_ file:
    * Add a Mutation for AddUser. It should use Mongoose to create a new user from the arguments supplied. You'll also need to create a token from the signToken utility that is already imported into this file. Then you need to return an object with both the token and the user, in that order.

In the client area, do the following:

* In the _client/src/App.js_ file:
    * Import all the necessary objects from the Apollo Client package. Also be sure to import ```setContext``` from the appropriate source.
    * Construct the main GraphQL entry endpoint
    * Insert a route that will respond to a path of "/saved" and will mount the SavedBooks component.

* In the _client/src/utils/mutations.js_ file, create a REMOVE_BOOK endpoint. (Hint: it will look fairly similar to the SAVE_BOOK endpoint above, but NOT THE SAME)

* In the _client/src/pages/SavedBooks.js_ file:
    * Import the two Apollo hooks you'll need. Hint: one is for queries, the other is for mutations.
    * Notice the two imports on lines 12 and 13. These are the GraphQL queries that will be run by this component.
    * Inside the SavedBooks method, call the QUERY_ME query and destructure the loading and data response properties. You're final line of code will look _similar_ to this:  ```const { var1, var2 } = useQuery(QUERY_ME)```

* In the _client/src/components/LoginForm.js_ file, do the following:
    * Call the QUERY_ME query and destructure the loading and data response properties. Your final query will look similar to this: ```const [var1, { var2 }] = useMutation(MUTATION_NAME_HERE);```

---
© 2021 Trilogy Education Services, LLC, a 2U, Inc. brand. Confidential and Proprietary. All Rights Reserved.
