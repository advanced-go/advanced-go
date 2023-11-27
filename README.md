# core

Core was inspired to capitalize on the Go language for application development. Determining the patterns that need to be employed is critical for writing clear idiomatic Go code. This YouTube video [Edward Muller - Go Anti-Patterns][emuller], does an excellent job of framing idiomatic go. 
[Robert Griesemer - The Evolution of Go][rgriesemer], @ 4:00 minutes, also presents an important analogy between Go modules, packages, closures, and LEGO® bricks. Reviewing the Go standard library packaging structure provides a blueprint for an application architecture, and underscores how essential package design is for idiomatic Go. 

Package dependencies also need to be obsessively managed. Rob Pike lists an important deign goal relating copying to dependency in [Go Proverbs][rpike], #8. Larger dependencies can be imported for test only to insure that the copied code is correct. Kent Beck's book on [Test Driven Development][kbeck], states, "Dependency is the key problem in software development of all scales." Lessening dependencies reduces complexity and increases reliability. [Doug McIlroy][dmcilroy] describes the early approach taken at Bell Labs when developing and revising [Research Unix][runix]: 

            We used to sit around in the Unix Room saying, 'What can we throw out? Why is there this option?' It's often because there 
	    is some deficiency in the basic design — you didn't really hit the right design point. Instead of adding an option, think 
	    about what was forcing you to add that option.

With the release of Go generics, a new paradigm has emerged: generic behaviors. Generic behaviors refere to the ability to use a type parameter to modify the behavoir of a function. Semantically, the type parameters that convey behaviors can be analogous to the "control plane" concept, and the type parameters the refer to data can be analogous to the "data plane" concept. The documentation below referes to all generic functions as templated, which is the implementation of generic programming from C++. The term templated is used to convey a wider meaning, encompessing both behavior and data type parameters.

What follows is a description of the packages in Core, highlighting specific patterns and template implementations.  



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
