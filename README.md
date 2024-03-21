# Advanced Go

Advanced Go is an exercise in creating [a better way to write software][robpike], by extending REST from the service/HTTP layer to the application layer. The following goals are examined when applying REST to packages, error handling, URLs, and testing. <!-- Go is a project to make building production software easier and more productive. -->

1. Reduce complexity
2. Reduce toil
3. Increase solution expressiveness   

 
## REST Applied to Packages
The [uniform interface for a package][exampledomain] simplifies the overall system architecture and increases the visibility of interactions. Expressiveness is enhanced in the following areas:
1. Composition of packages - Supported via the uniform interface, and also allows packages to be used as intermediaries for functinality such as authorization and access logging.
2. Microservice development - Packages are developed independently of hosts, allowing a package to exist in multiple hosts independent of different cloud hosting options. Toil is reduced as packages are fully tested in development, not requiring additional testing in a service.
3. [Mobile Code Architectural Style][rest] - Packages are independent of services, providing a dynamic service topography where reliability and latency can be managed by combining packages in a single service.

A package implementation also follows the [REST constraints][rest] of:
1. Resource identifier - PkgPath
2. Manipulation through representation - http.Request and http.Response
3. Self descriptive message - http.Request and http.Response

<!--Expressiveness - ability to compose resources/packages from already tested packages. Dynamic topography, mobile code.
Funcionality like authorization, access logging, via intermediaries
Seperation of concerns, host from application, other Cloud hosting options - less complexity, more expressiveness.
-->

## REST Applied to Error Handling 
Expressiveness - 
1. Uniform interface - ErrorHandler and logging. loging interface allows expresiveness
2. Constraints - resource identifier - PkgPath, manipulation through representation, and self descriptive message. http.Request and Http.Response
[Error handling][errorhandler] [generice type's][loghandler] for implementation.
Expressiveness through gnerics 

[Access logging][logger] also has a uniform Log function.  Expressive - Add traffic differentiation, ingress, egress, and internal

## REST Applied to URLs and Testing
Uniform interface - Resolver build with configurable templates. Expressiveness - Configurable templates to handle different URL resolution for development envirnment
URL as a resource


Treating a URL as a resource, where manipulation of the URL is through a representation, allows for that representation to change based on runtime environment/time. A [resolver type][resolver], provides the representations of a URL, and is the mechanism used to generate file scheme URL (file://) for testing and HTTPS scheme URL (https://) for runtime environments.


## REST Uniform Interface, Resource Identifier, & Self-Descriptive Messages
A key concept of REST is the uniform interface. A [package's][domainservice] HttpHandler implements that uniform interface, uses the http.Request type and allows easy integration with other packages. A package also includes a PkgPath that is used as an identifier for routing and error tracing.

The messaging package provides a [uniform interface][msgsend], [self-descriptive message][msgcore], and [resource identification][msgcore] for communication between resources using goroutines and Go channels. Functionality supported by messaging include startup, shutdown, and package health checks.



## REST Intermediaries
REST defines a layered architecture style where RESTful components can be easily connected via HTTP. Service authentication/authorization functionality is implemented by adding an [intermediary][intermediary].


## Testing
Testing utilizes a package's HttpHandler to test all requests and related responses. The requests and responses are HTTP text files, deserialized from disk into the appropriate [http.Request][httprequest] and [http.Response][httpresponse] types. This allows an automated, easy to extend solution for testing. Since the package HttpHandler is the public interface for the package, no further testing of the package needs to be done in a host.  

## Application Development
Development is streamlined as applications can be composed of existing resources/packages or resources in existing services. 

[robpike]: <https://thenewstack.io/golang-co-creator-rob-pike-what-go-got-right-and-wrong>
[rest]: <https://ics.uci.edu/~fielding/pubs/dissertation/fielding_dissertation.pdf>
[exampledomain]: <https://pkg.go.dev/github.com/advanced-go/example-domain/service>
[errorhandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#ErrorHandler>
[loghandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#Log>
[msgcore]: <https://pkg.go.dev/github.com/advanced-go/core/messaging#Message>
[msgsend]: <https://pkg.go.dev/github.com/advanced-go/core/messaging#SendFunc>
[domainservice]: <https://pkg.go.dev/github.com/advanced-go/example-domain/service>
[logger]: <https://pkg.go.dev/github.com/advanced-go/core/access#Log>
[intermediary]: <https://pkg.go.dev/github.com/advanced-go/core/host#ServeHTTPFunc>
[httprequest]: <https://pkg.go.dev/net/http#Request>
[httpresponse]: <https://pkg.go.dev/net/http#Response>
[resolver]: <https://pkg.go.dev/github.com/advanced-go/core/uri#Resolver>

<!--
### Hi there 👋


**advanced-go/advanced-go** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
