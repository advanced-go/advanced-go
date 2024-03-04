# Advanced Go

Advanced Go is an exercise in creating a new software engineering paradigm that would streamline application development, improve testing efficacy, and alleviate some of the things that are hard to change with a microservices architecture. This solution to creating a new paradigm was extending REST from the service/HTTP layer to the application layer. What follows are the implementation details of a new software engineering paradigm.

## REST Uniform Interface & Resource Identifier
A key concept of REST is the uniform inerface. A [package's][packagepkg] HttpHandler implements that uniform interaface, and allows easy integration with other package, either in process or via HTTP. A package also includes a PkgPath that can be used as an identifier

[Error handling][corepkg] also benefits from a uniform interface, adding a generice type for implementation. 
Access logging also has a uniform Log function.  




Additional [core][corepkg] modules was created to provide high levels of reliability and visibailty for AI Agent architectures.

[Messaging][messagingpkg] was developmented to provied ease of interactions between a network of heterogenous agents, working together satisify the goals of an AI Agent.



[aima]: <https://aima.cs.berkeley.edu/>
[corepkg]: <https://pkg.go.dev/github.com/advanced-go/core>
[messagingpkg]: <https://pkg.go.dev/github.com/advanced-go/messaging>
[packagepkg]: <https://pkg.go.dev/github.com/advanced-go/example-domain/service>

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
