# Advanced Go

Advanced Go is an exercise in creating a new software engineering paradigm that would streamline application development, improve testing efficacy, and alleviate some of the things that are hard to change with a microservices architecture. This solution to creating a new paradigm was extending REST from the service/HTTP layer to the application layer. What follows are the implementation details of a new software engineering paradigm.

## REST Uniform Interface & Resource Identifier
A key concept of REST is the uniform inerface. A [package's][domainservice] HttpHandler implements that uniform interaface, and allows easy integration with other packages.A package also includes a PkgPath that can be used as an identifier

[Error handling][errorhandler] also benefits from a uniform interface, allowing [generice type's][loghandler] for implementation. 

[Access logging][logger] also has a uniform Log function.  


## REST Intermediaries
REST defines a layered architecture style where RESTful components can be easily connected via HTTP. Service authenticaion/authorization are implemented by adding an [intermediary][intermediary].


[Messaging][messagingpkg] was developmented to provied ease of interactions between a network of heterogenous agents, working together satisify the goals of an AI Agent.



[aima]: <https://aima.cs.berkeley.edu/>
[errorhandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#ErrorHandler>
[loghandler]: <https://pkg.go.dev/github.com/advanced-go/core/runtime#Log>
[messagingpkg]: <https://pkg.go.dev/github.com/advanced-go/messaging>
[domainservice]: <https://pkg.go.dev/github.com/advanced-go/example-domain/service>
[logger]: <https://pkg.go.dev/github.com/advanced-go/core/access#Log>
[intermediary]: <https://pkg.go.dev/github.com/advanced-go/core/host#ServeHTTPFunc>

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
