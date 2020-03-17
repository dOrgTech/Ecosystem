# RFC-04: Documentation overhaul

## User Story

### Current
Trying to develop on alchemy is a complicated task, since is a pretty robust dApp. Users that are new to this software are more likely to have a hard time finding how they can get their local environment set up, and even more, trying to customizing it at their needs (Like playing with their own DAOs with their own schemes). This is because there's no simple documentation to guide the hacker to develop the app in an easy way. Currently, what dev does:

- Goes to alchemy repository, which has it's own [documentation](https://github.com/daostack/alchemy/tree/dev/docs) 
- The previous documentation it's hard to understand (Why? Because there's no a clear path to take) and the user doesn't know where to start. We should clarify what are the different case of uses and how you should start your local environment.
- There's no mention of hackers kit so some users don't even know it exists

### New 

As a developer I want to go to alchemy and see a good documentation, so I can save time and just go to tackle the problem I came to resolve, this way I dont need to understand the entire app to build a functionality.

## Detailed Design

We want to make a clear and easy to understand documentation.

First of all, remove the documentation from the Alchemy repository and make the DAO Hackers kit the only source of truth of how to develop on Alchemy, this way, if there's a modification, we only edit the hackers kit, making it easier to avoid misinformation between the Alchemy repository doc and the hackers kit.

This leads us to create an explicit documentation:
- We will create a specific section for alchemy development in [hackers kit](https://daostack.github.io/DAOstack-Hackers-Kit/gettingStarted/setupAlchemyDevMode/) (or a new alchemy hackers kit) which needs minor updates
  - Update commands (i.e: `docker compose`)
  - Can I run alchemy succesfully without docker? If so, how?
  - I know how to add a DAO into my local subgraph, but how to add/remove schemes?
  - How to run integration tests? Do I need to run alchemy locally first and then run the `npm run test:ingregrations` command?
- How to add a new generic scheme to an already deployed DAO.
   - It's unclear how to really set the voting machine parameters, there's no a clear indication of how the parameters should be added into the voting machine (i.e: Which order, what are the validations on the contract)
   - When creating the PR into the subgraph, how can I query the data of my DAO (Controller, DAOToken, Reputation and Arc Version) to add it into the file i'm creating 



## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 10 days | 1.0 FT | Create/edit alchemy hackers kit section, add the documentation of the alchemy's repository into this doc; making it more intuitive and easier to work on. Separating it into different sub sections, which are going to be: Set up/Development/Upgrades/Tests.

What are we going to show on each subsection?

Set up: How to start your local environment and how you can work with ganache (local) or rinkeby (testnet). Starting up your own subgraph or working with docker? Why and when do what (Depending on developer objective)

Development: Add a DAO to your local subgraph, as well as adding and removing schemes into already existing DAOs

Upgrades: Create a new generic scheme and add it into your DAO 

Tests: How to set up you environment to run integration tests

We want to create video tutorials for: 
- Deploying new generic scheme on remix and calling the method initialize (How to get the code of the generic scheme and the contracts it depends)
- How to add voting configuration into voting machine using remix
|

## Open Questions

Are we missing something?

## Impact on Adoption

This will allow a lot more of developer to have an easier development and the dApp will grow and be more robust faster