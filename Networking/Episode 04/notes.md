`REST API`

* Architecture
 1-tier Architecture :- whole code and FE, BE and storage is in one place
 2-tier Architecture :- FE and BE are separate
 3-tier Architecture :- FE, BE and storage are separate

API - Application Programming Interface
REST - Representational State Transfer

REST is build on HTTP( HYperText Transfer Protocol)

*  REST API (Representational State Transfer Application Programming Interface) is a way for different systems to communicate with each other over the web by using HTTP protocols, typically following a set of architectural constraints. It's one of the most common methods for building APIs (Application Programming Interfaces) that enable web services and applications to interact with servers, databases, or other external systems.

* Advantages of REST APIs:
 1. Stateless: No state is stored between requests, meaning each request must include all necessary information (authentication, resource identifier, etc.).
 2. Scalability: Statelessness and a uniform interface make REST APIs scalable.
 3. Flexibility (Ease of Use): Can be used with a wide range of programming languages and platforms.
 4. Uniform Interface: from Url you can understand what is this for
 5. Cacheable: Responses can be cached, improving performance.
 6. Separation of Concerns: FE or BE can be independent
 7. Interoperability:- Language agnostic(FE and BE can be written in any language)
 8. Ease of Testing
 9. Security

- REST APIs are widely used due to their simplicity, efficiency, and ability to integrate different systems over the web.

* Building Blocks of REST API
 1. URL(Uniform Resource Locator)
 2. Methods
 3. Headers
 4. Request
 5. Response
 6. Status Code

* `URL (Uniform Resource Locator)`
https://api.example.com/v1/users/123/posts?sort=desc&limit=10#top

1. Protocol (Scheme): https://

 This specifies the protocol used for communication between the client and the server. In this case, https stands for Hypertext Transfer Protocol Secure, which is the secure version of HTTP. Some APIs may use http (though https is preferred for security).

2. Host (Domain): api.example.com

 This is the domain name or IP address of the server that hosts the API. The domain (example.com) points to the specific service provider, and api is a subdomain used to indicate the API portion of the website.
 - SubDomain :- api or www
 - domain :- example
 - TLD(Top level Domain) :- com

3. Version: /v1

 APIs often have versioning to manage different versions of the API as it evolves over time. v1 refers to version 1 of the API. Other versions might be v2, v1.1, etc. This allows the API provider to introduce new changes without breaking existing applications that depend on older versions.

4. Resource Path: /users/123/posts

 This part specifies the resources or entities being accessed or manipulated:
 - /users: Refers to the collection of user resources.
 - /123: Refers to a specific resource (in this case, the user with ID 123).
 - /posts: Refers to the sub-resource (posts) related to the user. This implies that the request is focused on posts that belong to the user with ID 123.
 This hierarchical structure reflects how RESTful URLs organize resources and their relationships.

5. Query Parameters: ?sort=desc&limit=10

 Query parameters provide additional filtering or sorting options to refine the data returned by the API. They are appended to the URL after a ? symbol. (key value pair)
 - sort=desc: A query parameter used to specify that the list of posts should be sorted in descending order (probably by date).
 - limit=10: A query parameter used to limit the number of results returned to 10.
 Multiple query parameters are separated by an ampersand (&).

6. HTTP Method (Not shown in the URL but important):

 REST APIs use HTTP methods to specify the action being taken on the resource.
 - GET: To retrieve data (e.g., retrieve a user's posts).
 - POST: To create new data (e.g., create a new post for a user).
 - PUT/PATCH: To update existing data (e.g., update a user’s post).
 - DELETE: To delete data (e.g., delete a user’s post).
 The method determines how the API will process the request.

7. Fragment: #top
 
 these are used to store the extra information in the url
 hash(#) do not go from client to server
 for eq:- scroll position here