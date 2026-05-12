#### Why this project?
Since this is a existing project, reused by a lot of students. Me, one among them. Let me note down everything I learnt from this.

#### Monolithic Arch vs Micro Services:
The former means that the whole application will be a single codebase, meaning the whole project shares the same tech stack and versions shared. 

###### Pros:
- Easy to maintain and Build
- ownership is maintained by one
- communication between different modules is easy
- Easier for small scale projects and systems

###### Cons:
- To heavy when we have multiple modules.
- Minor changes require whole project to be redeployed
- Scaling up/down a specific module is inflexible
- Changes and version updates may break non related components as everything is tightly coupled.
  
###### note:
Reminding myself to practice reading code faster and better. This project was well structured but still took a while to understand everything. Not on ownership level but I need to be good enough to work on someone else codebase.
#### Also relearnt Markdown again lol
`#` symbols (1-6) for heading levels. `# H1` `## H2`

`*text*` or `_text_` for _italics_, 

`**text**` or `__text__` for **bold**,  

`~~text~~` for ~~strikethrough~~. 

- Unordered: `- item` or `* item`
- Ordered: `1. item`
- Checklists: `- [ ] task` or `- [x] completed`

backticks for inline code `` `code` `` and triple backticks for code blocks.

```
    print("Hello")
```

`[text](url)` for inline links and `![alt](url)` for images. 

`> text` to create quoted sections.

three or more hyphens `---`, asterisks `***`, or underscores `___` on a line by themselves. 

 `\` to escape special characters like `*`, `_`, or `#`.

#### Git Repo and .gitignore
So on major thing I forgot was that not everything is to be saved in my repo. Previously we only sent core files since the CM team took care of the build, but as a Solo developer I need to understand and also keep note of the CI/CD Devops pipelines. 
So what files to include and what to ignore? kinda confusing but let's try understanding.
This is a MERN stack Monolith so the build files will include node modules, archives, credentials, logs, build outputs and compiled files and foremost the env files too. All these are included in the .gitignore file.

#### URLS Setup
Hardcoding URLs are a easy way for local env Runs but in the long run it will cause me issues when I Containerize or host the projects. The better way I learnt is to create local .env variables and dynamically pass the URLs across the files.

Note: to make sure the user/container knows what the .env files should have we create a .env.example with dummy values that will be pushed to repo.

#### Payments
Stripe is one gateway partner. Easy to use too. Made an Account and set the Env to sandbox for testing. Then from the API keys, took the secret key and saved it in my .env file since everything else is handled in the project. This means we are able to place orders now.

#### Mongo Clusters
So we have the mongo cluster (cluster0) and DB (tomato-db) used here. We can get that info from the connection link. Or if in case needed, we can change the link to point the DB of our choice.

## Note
This Project is a working Monolithic project that can be run on your own system. Follow the Readme for more info.