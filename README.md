# Advanced Go

Advanced Go is an exercise in creating a new software engineering paradigm that would streamline application development, improve testing efficacy, and alleviate some of the things that are hard to change with a microservices architecture. This solution to creating a new paradigm was extending REST from the service/HTTP layer to the application layer. What follows are the implementation details of a new software engineering paradigm.

## REST Uniform Interface, Resource Identifier, & Self-Descriptive Messages
A key concept of REST is the uniform inerface. A [package's][domainservice] HttpHandler implements that uniform interaface, uses the http.Request type and allows easy integration with other packages. A package also includes a PkgPath that is used as an identifier

The [messaging][messagingcore] package provides a uniform interface, self-descriptive message, and resource identification for communication between resources
using goroutines and gochannels. Functionality supported by messaging include startup, shutdown, and package health check.

[Error handling][errorhandler] also benefits from a uniform interface, allowing [generice type's][loghandler] for implementation. 

[Access logging][logger] also has a uniform Log function.  

## REST Intermediaries
REST defines a layered architecture style where RESTful components can be easily connected via HTTP. Service authenticaion/authorization functionality is implemented by adding an [intermediary][intermediary].

## URL as a Resource

## Testing
Testing utilizes a package's HttpHandler to test all requests and related responses. The requests and responses are HTTP text files, deserialized from disk into the appropriate [http.Request][httprequest] and [http.Response][httpresponse] types. This allows an automated, easy to extend solution for testing. Since the package HttpHandler is the public interface for the package, no further testing of the package needs to be done in a host.  

## Application Development


[errorhandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#ErrorHandler>
[loghandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#Log>
[messagingcore]: <https://pkg.go.dev/github.com/advanced-go/messaging#Message>
[domainservice]: <https://pkg.go.dev/github.com/advanced-go/example-domain/service>
[logger]: <https://pkg.go.dev/github.com/advanced-go/core/access#Log>
[intermediary]: <https://pkg.go.dev/github.com/advanced-go/core/host#ServeHTTPFunc>
[httprequest]: <https://pkg.go.dev/net/http#Request>
[httpresponse]: <https://pkg.go.dev/net/http#Response>

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
