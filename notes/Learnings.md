Since this is a existing project, reused by a lot of students. Me, one among them. Let me note down everything I learnt from this.

##Monolithic Arch vs Micro Services:
The former means that the whole application will be a single codebase, meaning the whole project shares the same tech stack and versions shared. 
Pros:
- Easy to maintain and Build
- ownership is maintained by one
- communication between different modules is easy
- Easier for small scale projects and systems
Cons:
- To heavy is we have multiple modules.
- Minor changes require whole project to be redeployed
- Scaling up/down a specific module is inflexible
- Changes and version updates may break non related components as everything is tightly coupled.