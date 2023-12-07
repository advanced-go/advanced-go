# Advanced Go

Advanced Go is an exercise in development of architectures to facilitate the development of AI Agents. Inspiration for the AI Agent architecture is defined in the AI text book by [Stuart Russell & Peter Norvig][aima]. The textbook defines an AI Agent as follows:
~~~
An agent is anything that can be viewed as perceiving its environment through sensors and acting upon that environment
through effectors. 
~~~

The AI Agent developed implements an observation -> analyze -> act cycle focused on autonomous 

The agent utilizes the following modules:

1. example-agent - resiliency agent implementation
2. example-domain - resources used by the agent: timeseries access log, SLO, and an agent activity audit trail
3. example-host - a service host for the AI Agent
4. example-test - a test application used to send timeseries and SLO data to the service host.

Additional [core][corepkg] modules was created to provide high levels of reliability and visibailty for AI Agent architectures.

[Messaging][messagingpkg] was developmented to provied ease of interactions between a network of heterogenous agents, working together satisify the goals of an AI Agent.



[aima]: <https://aima.cs.berkeley.edu/>
[corepkg]: <https://pkg.go.dev/github.com/advanced-go/core>
[messagingpkg]: <https://pkg.go.dev/github.com/advanced-go/messaging>

### Hi there 👋

<!--
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
