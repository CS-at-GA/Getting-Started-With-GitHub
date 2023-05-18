Project Management With GitHub
====
```mermaid
sequenceDiagram
    actor You
    participant replit
    participant repository
    participant GitHub
    Note over You,GitHub: setting up your project
    You -->> replit: make a replit for your project
    replit -->> repository: make repository
    repository -->> GitHub: sync repository
    Note over You,GitHub: project management setup
    You -->> GitHub: create a github project
    You -->> GitHub: create an issue for your project and associate it with your github project
    You -->> GitHub: create open list items for each task
    Note over You,GitHub: Workflow
    You -->> GitHub: before starting, create an issue for the task
    You -->> GitHub: create open list items for each sub-task
    You -->> GitHub: (optional) create a branch for the task
    replit -->> repository: (optional) switch to branch
    loop Every incomplete issue
        loop code
            You-->>replit: write code
            replit-->>You: test
        end
        Note over You,replit: when something works
        replit-->>repository: commit
        repository-->>GitHub: push
        You-->>GitHub: mark issue as complete
    end
```
