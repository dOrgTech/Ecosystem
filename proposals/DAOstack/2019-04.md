# Milestone 1 Deliverables

Date: Apr 26, 2019

*An overview of dOrg's progress in the first 2-month segment of our partnership with DAOstack (March 1 - April 30)*

### Summary of Document:

- DAOcreator
- DAOcomponents
- DAOregistry
- BBLLC
- Self-Sustainability
- Summary of Future Work

# DAOcreator (v0.2)

### Front-End

We've made a lot of progress updating and refining the DAOcreator, both in UX and functionality. The latest version [can be viewed here](https://dorg.tech). 

- Change Log:
    - Remove Arc.js Dependency
    - Enable Mainnet Deployments
    - Configurable Voting Machines
    - Configurable Schemes
    - Scheme Specific Voting Machines
    - Helpful Descriptions
    - Input Validation
    - User Friendly Transaction Descriptions
    - New User Landing Page
    - Notification Refinement
    - Bug Fixes++

### Back-End

In order for Alchemy to support these newly deployed DAOs, the subgraph needs to be updated to use a new feature that has just been released from The Graph Protocol. This new feature is called "Dynamic Datasources" or "Template Datasources". We performed some preliminary R&D to help move this update along. When this feature is integrated into DAOstack's subgraph, DAOs created with DAOcreator will show up and be usable in Alchemy.

- [Issue](https://github.com/daostack/subgraph/issues/197)
- [WIP Implementation](https://github.com/dOrgTech/subgraph/pull/2)

# DAOcomponents

### Present (POC)

DAOcomponents aims to create an easy to use React Component Library that wraps the DAOstack/client library. The hope is to be able to turn any app into a DAO enabled dApp by adding ~2 components.

- For more information on how to use the library, please refer to the [README](https://github.com/dOrgTech/DAOcomponents/blob/master/README.md)
- The library is almost ready for Proof-of-Concept release. [View the remaining tasks for POC release here](https://github.com/dOrgTech/DAOcomponents/milestone/1).
- Additionally, Genesis DAO has signaled its interest in the project. [See passed proposal here](https://alchemy.daostack.io/dao/0x294f999356ed03347c7a23bcbcf8d33fa41dc830/proposal/0xca25582de4148b1c960d3d32fd96a1b017b9c3757c8165e2343a54c5b8425329).

### Future (MVP)

Future plans for this project are:

- Onboard Shiv who's expressed interest in helping with further development
- Finish POC milestone and publish to NPM
- DAOexplorer integration
- Start developing dOrg's front-end for Arc
- Alchemy integration?

[See the full list of features for the MVP release here](https://github.com/dOrgTech/DAOcomponents/milestone/2https://github.com/dOrgTech/DAOcomponents/milestone/2).

# DAOregistry

The DAOregistry is a whitelist of DAOs to be curated by the Genesis DAO. In DAOstack's current [implementation](https://github.com/daostack/arc-hive/blob/master/contracts/DAORegistry.sol), the Genesis Avatar would own the registry contract. We implemented a scheme that interfaces with this registry using a generic action call.

Check out our

- [DAORegistryScheme implementation](https://github.com/dOrgTech/arc-hive/blob/dao-registry-scheme/contracts/DAORegistryScheme.sol)
- [New specification](https://gist.github.com/gh1dra/7bd7cb0700d81b474ed0b79d81f5b30d)
- [Pull Request](https://github.com/daostack/arc-hive/pull/9) awaiting final approval

# BBLLC

The Blockchain-Based Limited Liability Company is a new legal entity classification in Vermont which allows a company to govern and operate itself on a blockchain. We believe that this law and others like it present possible "legal solutions" for DAOs.

To this end, we established an engagement with local advisors who assisted with the development of Vermont's BBLLC law to develop:

1. A legal wrapper for dOrg's DAO
2. Guidelines and templates for DAOs to seamlessly register their own legal wrappers. See [here](https://docs.google.com/document/d/18gfexutgAVBpEpCyDg2e0XvudLNpZ-sjfp3gYQVesR4/edit#) for more info

So far, we have worked with our legal counsel to draft the initial set of legal agreements for dOrg's BBLLC-DAO (Operating Agreement, Contractor Agreements, etc). The entity will be registered within the next 1-2 weeks.

Going forward, we plan to work on:

- Templating software to automate generation and execution of the relevant legal contracts for new DAOs
- Integrating this functionality into the DAOcreator wizard
- Templating and integrating other legal entity classifications

# Self Sustainability

### Grants

**Gnosis GECO**: Awarded grant to work on Continuous Funding Scheme for the dxDAO.

- [Original Proposal](https://github.com/gnosis/GECO/pull/29https://github.com/gnosis/GECO/pull/29)
- [Presentation Slide Deck](https://docs.google.com/presentation/d/18psmeqqw0fJdfs1iuVA7DHtCDrVSX8Fkm32MvHYXDgI/edit?usp=sharing)
- [Acceptance Video](https://youtu.be/LB_E8OqMxzE)

### Potential Clients

We have also been scoping out projects with clients who would pay us to build particular DAOstack integrations.

# Summary of Future Work

### DAOcreator

- Finish up R&D on Subgraph Datasource Templates needed to add Alchemy Earth support for newly deployed DAOs
- Release v0.3
    - Additional [bug fixes and usability improvements](https://github.com/dOrgTech/DAOcreator/issues)
    - Additional features, including DAOregistry support and legal entity registration

### DAOcomponents

- Finalize [POC](https://github.com/dOrgTech/DAOcomponents/milestone/1)
- Work towards [MVP](https://github.com/dOrgTech/DAOcomponents/milestone/2)

### DAOregistry

- Finalize DAORegistryScheme implementation

### BBLLC

- Finalize legal entity registration

### Continuous DAOs

- begin work on Gnosis GECO project

### Self-Sustainability

- Close additional grants and clients