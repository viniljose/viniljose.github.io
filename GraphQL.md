GraphQL is a query language for your APIs. It’s also a runtime for fulfilling queries with your data. The GraphQL service is transport agnostic but is typically served over HTTP.
GraphQL is a specification (spec) for client-server communication.
Design Principles of GraphQL:
Hierarchical:A GraphQL query is hierarchical. Fields are nested within other fields and the query is shaped like the data that it returns.
Product centric:GraphQL is driven by the data needs of the client and the language and runtime that support the client.
Strong typing:A GraphQL server is backed by the GraphQL type system. In the schema, each data point has a specific type against which it will be validated.
Client-specified queries:A GraphQL server provides the capabilities that the clients are allowed to consume.
Introspective:The GraphQL language is able to query the GraphQL server’s type system.

Some Rest Draw Backs:
overfetching—we’re getting a lot of data back that we don’t need.We ask for only the fields that we want.
Underfetching-The GraphQL solution to underfetching is to define a nested query and then request the data all in one fetch.
Managing REST Endpoints-With GraphQL, the typical architecture involves a single endpoint. The single endpoint can act as a gateway and orchestrate several data sources, but the one endpoint still makes organization of data easier.

GraphQL Query Language:GraphQL and SQL also have entirely different syntax. Instead of SELECT, GraphQL uses Query to request data. This operation is at the heart of everything we do with GraphQL. Instead of INSERT, UPDATE, or DELETE, GraphQL wraps all of these data changes into one data type: the Mutation. Because GraphQL is built for the internet, it includes a Subscription type that can be used to listen for data changes over socket connections.

GraphiQL is the in-browser integrated development environment (IDE) that was created at Facebook to allow you to query and explore a GraphQL API. GraphiQL offers syntax highlighting, code completion, and error warnings, and it lets you run and view query results directly in the browser. 
Successful queries return a JSON document that contains a “data” key. Unsuccessful queries return a JSON document that contains an “errors” key. The details of what went wrong is passed as JSON data under this key. A JSON response can contain both “data” and “errors.”

Subscriptions
The third type of operation available with GraphQL is the subscription. There are times when a client might want to have real-time updates pushed from the server. A subscription allows us to listen to the GraphQL API for real-time data changes.
Subscriptions in GraphQL came from a real-life use case at Facebook. The team wanted a way to show real-time information about the number of likes (Live Likes) that a post was getting without refreshing the page. Live Likes are a real-time use case that is powered by subscriptions. Every client is subscribed to the like event and sees likes being updated in real time.
