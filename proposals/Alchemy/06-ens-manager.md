# RFC-06: ENS Manager

## User Story

### Current

  DAOs does not have any way to interact with their ENS domains (if they have) - Or the ability to create an ENS (after ENS plugin has been added)

### New 

  User can go to a section of "ENS Dashboard" in DAO, where he can manage all the domains that are owned by the organization, if he wants to make a change it will need to go through a proposal on ENS plugin.

  If the ENS Dashboard is not added, there will be a button on this section that will create the proposal in scheme manager to add this new scheme

## Detailed Design

  We want to interact with the ENS contracts, so the DAO can registrer/edit/renew it's domains by interacting with the ENS contracts.

  The integration consists on two steps, which are going to be:
  - Dashboard UI
  - Interacting with ENS Contracts
    - Resolving ENS Names: This will allow DAO to understand ENS Names, meaning that, a user can create a proposal and the recipient can be an ENS name like `cesar.eth`
    - Support Reverse Resolution: DAO will display ENS Name wherever it displays an address (DAO members, or proposal) - If the address has an ENS name associated
    - Name registration/Name updates: User can register and/or update an existing ENS


## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 2 weeks | 1.0 FT | Dashboard UI: We are going to create a new section, which can be accessed through the side bar, it will be a table with the ENS already registered to the DAO address and it will have buttons to create (register) new ENS names |
| 2 weeks | 1.0 FT | Develop the interaction with ENS contracts, so the dashboard can use this methods |

## Open Questions

None
