# RFC-01: Generic Actions Tooling

## User Story

### Current

Adding GA plugins within Alchemy currently has the following problems:  
- No UI for configuring & deploying a new GA plugin contract – must be done by a skilled programmer.
- No UI for knowing what types of GAs Alchemy supports (ENS Registrar, Uniswap, etc).
- No UI for creating new types of GAs that Alchemy can support (Compound, etc) – must be PR'd into Alchemy for them to be usable.
- Complex UI for adding a GA plugin to the DAO via the plugin manager.
- Subgraph does not pickup on newly deployed GA plugin contracts.

### New

As a DAO founder or enthusiast I want to easily interface my DAO with existing smart contracts, so that it can perform particular actions (set parameters, manage finances).

As a protocol developer, I want to give DAOstack DAOs the ability to interact with my smart contracts (ENS, Uniswap, Compound), so that adoption of my protocol increases.

## Detailed Design

### Terminology

**GA Creator**: UI for configuring & deploying new generic action plugins from within Alchemy. Deployment via the UI will (1) deploy a new GA plugin contract via the ***GA Factory*** and (2) call create a proposal in the DAO's Plugin Manager to add the new GA plugin.  
**GA Factory**: Contract factory that spawns new GA plugin contracts. This is needed until Arc-Hives is live.  
**GA Designer**: UI for defining new generic actions (Compound, Uniswap, Moloch, etc). The UI will be a front-end for defining [GA JSON files](https://github.com/daostack/alchemy/tree/dev/src/genericSchemeRegistry/schemes), and proposing them to the ***GA Registry***.  
**GA Registry**: On-chain registry of GA JSONs. This registry should be managed by a DAO made up by the stake-holders of Alchemy. The Alchemy DAO.  
**Known GA**: A Generic Action that's registered in the registry.  

This is the main section of the RFC. What does the proposal include? What are
the proposed interfaces/APIs? How are different affected parties, such as users,
developers or node operators affected by the change and how are they going to
use it?

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 1 Month | 1.0 FT | TODO |
| 1 Month | 1.0 FT | TODO |

## Open Questions

- How will this feature be affected by Stack 2.0 changes?

- Would it be better to focus on creating a "generic generic action" rather than encouraging a proliferation of particular generic actions?

## Impact on Adoption

The ability to easily call existing smart contracts is crucial for adoption by any Ethereum projects interested in DAOifying their governance with DAOstack.

Many projects are currently choosing to use Aragon specifically because [Aragon Agent](https://aragon.org/agent/) makes it easy to interface their DAO with smart contracts.

This is a HUGE missed opportunity right now.
