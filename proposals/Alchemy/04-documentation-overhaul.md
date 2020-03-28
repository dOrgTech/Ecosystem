# RFC-04: Documentation overhaul

## User Story

### Current
Learning to develop new features and integrations for Alchemy is a complicated task. Developers that are new to this software commonly have a hard time finding how they can:
- setup their local environment
- how to add new functionality (generic actions)
- how to setup a test DAO
- how to modify the test DAO

This is partly because there is not a lot of simple documentation that can help guide the developer. Currently, developers can:
- Go to the Alchemy repository, which has its own [documentation](https://github.com/daostack/alchemy/tree/dev/docs).
- The previous documentation it's hard to understand (Why? Because there's no a clear path to take) and the user doesn't know where to start. We should clarify what are the different case of uses and how you should start your local environment.
- Additionally the alchemy documentation is out of date.
- There's no mention of Hackers Kit so some users don't even know it exists.

### New 

As a developer I want to go to Alchemy and see good documentation, so I can save time and just go to tackle the problem I came to resolve. This way I don't need to understand the entire app to build my functionality.

## Impact on Adoption

This will allow more developers to build on the stack, and improve the usability of the platform, making DAOstack more robust.

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 1 week | 2.0 FT | Improve Alchemy documentation, creating a simple step by step guide for new developers who'd like to modify or extend Alchemy, move this to the Hacker's Kit with additional learning materials. |

## Detailed Design

We want to make a clear and easy to understand documentation.

First of all, remove the documentation from the Alchemy repository and make the DAO Hackers Kit the only source of truth of how to develop on Alchemy, this way, if there's a modification, we only edit the Hackers Kit, making it easier to avoid misinformation between the two repositories.

The sections that will be covered are:
- Set up: How to start your local environment and how you can work with ganache (local) or rinkeby (testnet). Starting up your own subgraph or working with docker? Why and when do what (Depending on developer objective)

- Development: Add a DAO to your local subgraph, as well as adding and removing schemes into already existing DAOs

- Upgrades: Create a new generic scheme and add it into your DAO 

- Tests: How to set up you environment to run integration tests

## Open Questions
