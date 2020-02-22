# Milestone 2 Deliverables

Date: Jun 28, 2019

*An overview of dOrg's progress in the second 2-month segment of our partnership with DAOstack (May 1 - June 30)*

### Summary of Document:

- BBLLC
- DAOcreator - UI
- DAOcreator - Subgraph
- DAOcomponents
- DAOregistry
- Ecosystem
- Self-Sustainability

# BBLLC

Launched a blockchain-based LLC legal wrapper for the newly deployed dOrg DAO. 

### Present

- dOrg **DAO deployed**: First company to migrate all funds and operations to a DAOstack DAO
- dOrg **BBLLC formed**: First limited liability DAO (linked to a DAOstack DAO)
- **Press Attention**: DAOstack featured in news about our BBLLC
    - [Coindesk](https://www.coindesk.com/dorg-founders-have-created-the-first-limited-liability-dao)
    - [Cointelegraph](https://cointelegraph.com/news/dorg-llc-purports-to-be-first-legally-valid-dao-under-us-law)
    - [MIT Law](http://law.mit.edu/bbllc)
- DAO-specialized **legal agreements** finalized and [open-sourced](https://app.openlaw.io/template/bbllc-dao%20-%20vermont)
- **Operational Protocols** implemented for managing work-orders, invoices, legal agreements and Reputation through proposals

### Future

- Develop toolchain for integrating legal agreements into DAO proposal flow
    - "Legal Scheme" for legal decisions
    - IPFS storage solution for legal agreement versioning
    - Alchemy-embedded U.I. components
- Explore avenues for funding (Received initial interest from OpenLaw, Atrium and others)

# DAOcreator - UI

DAOcreator is a front-end for designing & deploying Arc-based DAOs.

### Present

After receiving feedback from the DAOstack team during our last milestone review, we chose to unprioritize development of DAOcreator. Some updates we made during this shelving period include:

- Mobile friendly [About](https://dorg.tech/#/about) & [FAQ](https://dorg.tech/#/overview) pages
- [Warning](https://dorg.tech/#/dapp) page
- [More robust deployment](https://github.com/dOrgTech/DAOcreator/commit/41640bcea1dcdc1a0a0005bd8b361eaa49e28eab), helping ensure transactions are resolved and don't time-out

### Future

We have decided to reprioritize the DAOcreator after receiving renewed interest and feedback on its importance over the last month. During this next phase, we plan on adding:

- "**Simple Mode**" where we'll hide all advanced features and present users a simple click by click tutorial for standing up a "Minimum Viable DAO"
- Additional warnings (or disabling) features that are unsupported by Alchemy
- "**Request U.I.**" instructions and submission form to request your newly deployed DAO be indexed by Alchemy's subgraph
- Serialization features where users can **import** pre-saved configurations ("templates"), and **export** their DAO's configuration to be used with the daostack/migration project

# DAOcreator - Subgraph

DAOs deployed with the DAOcreator are not able to be viewed in Alchemy due to the subgraph only supporting static contract addresses. We've worked towards solving this.

### Present

- [PR adding "**Data Source Template Support**" to the subgraph](https://github.com/daostack/subgraph/pull/215) is awaiting final approval
- [PR adding an "**On-Chain DAO-Indexing** Source of Truth" to Arc](https://github.com/daostack/arc/pull/640) is on stand-by
- [A solution that avoids DAOstack having to maintain a monolithic subgraph](https://github.com/daostack/subgraph/issues/270) is being explored.

### Future

- Since a solution for automatically indexing newly deployed DAOs has not been reached, we will smoothen the UX for new DAOs to request that their contract addresses be added to DAOstack's subgraph manually. We can add this to the final page of the DAOcreator
- A solution where dOrg stands up new caching servers for DAOs is a possibility
- Continue to hold conversations with the tech team until a clear path forward is found

# DAOcomponents

DAOcomponents aims to create an easy to use React Component Library that wraps the DAOstack/client library. The hope is to be able to turn any app into a DAO enabled dApp by adding ~2 components.

### Present

- Lots of continued work has taken place including...
    - **all major DAO primitives** have been added
    - component list **sorting** and **filtering** support
    - a blocking architectural flaw was [fixed](https://github.com/dOrgTech/DAOcomponents/commit/2a10b7f913f7760bd8bb213c0a6ddd0babe49eaf)
    - additional environment **debugging tools** for local development
- PRs and issues have been opened against DAOstack's Client library, as a few breaking changes and inconsistencies were found
    - PRs: [#190](https://github.com/daostack/client/pull/190), [#210](https://github.com/daostack/client/pull/210), [#211](https://github.com/daostack/client/pull/211), [#212](https://github.com/daostack/client/pull/212), [#228](https://github.com/daostack/client/pull/228), [#235](https://github.com/daostack/client/pull/235), [#246](https://github.com/daostack/client/pull/246)
    - Issues: [#234](https://github.com/daostack/client/issues/234), [#229](https://github.com/daostack/client/issues/229), [#227](https://github.com/daostack/client/issues/227), [#214](https://github.com/daostack/client/issues/214), [#213](https://github.com/daostack/client/issues/213), [#196](https://github.com/daostack/client/issues/196)
- [An alpha version was published to NPM](https://www.npmjs.com/package/@dorgtech/daocomponents)
- Shiv was on-boarded and...
    - helped with the continued development of the project
    - integrated DAOcomponents into **DAOexplorer**
    - provided valuable feedback
    - helped spec out future work items

### Future

- Continue to move towards a solid beta release
- Support Shiv in DAOexplorer development
- Create small sample applications

# DAOregistry

The DAOregistry is a whitelist of DAOs to be curated by the Genesis DAO. In DAOstack's current [implementation](https://github.com/daostack/arc-hive/blob/master/contracts/DAORegistry.sol), the Genesis Avatar would own the registry contract. We implemented a scheme that interfaces with this registry using a generic action call.

### Present

- **RegistryScheme tests** added
- [PR awaiting final approval](https://github.com/daostack/arc-hive/pull/9)

### Future

- Generic "RegistryScheme" Specification & Prototype
    - This scheme will allow a DAO to interact with any registry that implements the "ISerializableRegistry" interface
    - We plan to use this for our various registry DAO projects going forward: Token Registry, Identity Registry, DAO Registry, etc

# Ecosystem

### DAOify Hackathon

On-boarded new developers to the community and created reusable presentations about DAOstack.

- [DAOstack Tech Stack](https://docs.google.com/presentation/d/1x4bWuRRz9T0yqS-JeGX0SMeKiiK-g56Z7rbJeOYiDk4/)
- [DAOstack Ecosystem](https://docs.google.com/presentation/d/1rW7n8Cori9hN-rbJhge2onXdbfS_w9sAF-FGsFk61KI)
- Winning Projects:
    - [Predictor App](https://github.com/electrone901/predictor-app)
    - [Blockathon](https://alchemy.daostack.io/dao/0x294f999356ed03347c7a23bcbcf8d33fa41dc830/proposal/0xf673ccb4e1d2479d50797cf3850265ca0c50e93843239a9ef0353b14d7c6a59b) proposal
    - [WeatherCon](https://alchemy.daostack.io/dao/0x294f999356ed03347c7a23bcbcf8d33fa41dc830/proposal/0x84ccf3a53b112ebfe236bd1a3e2db030d23c16666d02cda0bd48648a99cce742) proposal

### Scheme Registrar Tutorial

[Helped Ezra author a "How To" article on the Scheme Registrar.](https://daotalk.org/t/how-to-use-the-scheme-registrar-in-alchemy/669) We created a step by step guide for updating Genesis Protocol parameters using Etherscan and Alchemy. 

### DAOstack R&D Resource List

[Authored this overview](https://daotalk.org/t/resource-list-dao-r-d/572) that can be used to help new open-source developers get started.

### On-boarded 4 New Developers

dOrg has on-boarded 4 new developers to help with ongoing projects, and in doing so they've been on-boarded into the DAOstack ecosystem.

- [Thomas Spofford](https://github.com/tspoff)
- [Seth Febius](https://github.com/sethfork)
- [Jeremy Luso](https://github.com/jvluso)
- [Luis Dominguez](https://github.com/luis-sh)

# Self-Sustainability

## Gnosis: Bonding Curves for DAOs

Bonding curve support for DAOs to allow continuous funding.

### Present

- Started May 20th
- Contracts for schemes and curve [prototyped](https://github.com/dOrgTech/BC-DAO/tree/master/contracts)
- Delivered [initial spec](https://github.com/dOrgTech/BC-DAO/) with overview of economic model and technical architecture
- Delivered [research survey](https://github.com/dOrgTech/BC-DAO/blob/master/research.md) of existing bonding curve projects

### Future

- Finalize economic model
- Fully implement and audit all contracts

## GoodDollar: Identity DAO

DAO-curated registry of human identities to be integrated with the GoodDollar app.

### Present

- Started June 17
- [Initial technical specification and product overview / UX flow drafted](https://drive.google.com/file/d/1NWTYfKECUuUD4yw3OMGJbKnL-aYmWo9y/view)
- Scheme and registry contracts prototyped

### Future

- Complete spec & mock-ups
- Implement all contracts and U.I. components
- Build javascript Web3 plug-in for easy application integration