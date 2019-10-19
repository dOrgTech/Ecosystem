# Milestone 3 Deliverables

Date: Aug 29, 2019
Tags: Deliverables,Milestone

*An overview of dOrg's progress in the third 2-month segment of our partnership with DAOstack (July 1 - August 31)*

*See here for [Milestone 1 Deliverables (March 1 - April 30)](https://www.notion.so/dorg/Milestone-1-Deliverables-5fead6b0a777440bb3830dcedb3f5fe0)

*See here for [Milestone 2 Deliverables (May 1 - June 30)](https://www.notion.so/dorg/Milestone-2-Deliverables-4bad3fec174048a9890f9d3a2459f66a)

### Summary of Document:

- DAOcreator - UI
- DAOcreator - Subgraph
- DAOcomponents
- Ecosystem
- Self-Sustainability

# DAOcreator - UI

DAOcreator is a front-end for designing & deploying Arc-based DAOs.

### Present

- Complete UI Overhaul

    [https://youtu.be/iKTuQT0bBf4](https://youtu.be/iKTuQT0bBf4)

    - Genesis Protocol Voting Machine Presets: Easy, Normal, Critical, Custom
        - Custom configurations screen with tailored field controls and tool-tips.
    - Member's CSV Import / Export
        - CSV Template Download
    - Export dao-params.json
    - Core Form Library
        - Complex Validation Logic
        - React Agnostic
        - Plan to ship this as its own package for other tools to use. We've talked with [Odyssy](https://odyssy.io/) about using it in their [DAOhaus](https://daohaus.club/) application and they were super interested.

### Future

- Mainnet Deployments
- Simple Mode + DAO Templates
- Reputation Bootstrapping Schemes
- Members Editor Redesign
- Import dao-params.json
- Persist sessions through local storage
- Use the core library in other applications ([Odyssy](https://odyssy.io/))

# DAOcreator - Subgraph

DAOs deployed with the DAOcreator are not able to be viewed in Alchemy due to the subgraph only supporting static contract addresses. We've worked towards solving this.

### Present

- [Subgraph PR](https://github.com/daostack/subgraph/pull/215) ready to be merged
- [DAOtracker PR](https://github.com/daostack/arc/pull/640) ready to be merged

### Future

- Integrate DAOtracker to the migration scripts
- Integrate DAOtracker to the subgraph
- 🙌 Deploy in DAOcreator → Use in Alchemy 🙌

# DAOcomponents

DAOcomponents aims to create an easy to use React Component Library that wraps the DAOstack/client library. The hope is to be able to turn any app into a DAO enabled dApp by adding ~2 components.

### Present

- Updated to latest client version
- Added the following components
    - Stake(s)
    - Scheme(s)
    - Token(s)
    - Vote(s)
- [Breaking issue](https://github.com/daostack/subgraph/issues/321) found where subgraph endpoints go offline
- [Improved loading handler](https://github.com/dOrgTech/DAOcomponents/commit/746f5ad8c714a9c58bca9ae82f836af7ff1fbac8)
- Improved ComponentList Inference [underway](https://github.com/dOrgTech/DAOcomponents/compare/infer-prop?expand=1)

        <Member address={"0xMy_Address"} daoAddress={"0xDAO"}>
          <Proposals from={"Member as proposer"}>
          ... all proposals created by this member

### Future

- Complete improved inference
- Support interested users
    - [DAOhaus](https://daohaus.club/)
    - New Alchemy

# Ecosystem

## Berlin Blockchain Week

dOrg members participated in various blockchain week events to share our progress with the rest of the ecosystem.

- **Web3Summit**: [Ori spoke at the dgov node](https://www.youtube.com/watch?v=-cW4HVLDCJ8) about how dOrg uses Alchemy to operate its legal entity.
- **DAOfest**:
    - [Jordan spoke](https://www.youtube.com/watch?v=XBjy4oj61JE) about DAOstack's tech stack and open source ecosystem.
    - [Ori spoke](https://www.youtube.com/watch?v=BTZMRR1YRyo) about dOrg's legal process.
- **Dappcon**: [Thomas spoke](https://www.youtube.com/watch?v=TTk-I7QmBm0) about dOrg's bonding curves for DAOs project.
- **ETHBerlin**: Enjoyed good company and conversation.

## On-boarded 7 New Developers

dOrg has on-boarded 7 new developers to help with ongoing projects, and in doing so they've been on-boarded into the DAOstack ecosystem.

- [Bogdan](https://github.com/bogdanbatog) - Adding a scalable dividend solution to the [Bonding Curve DAO](https://github.com/dorgtech/bc-dao) project.
- [Christian](https://github.com/xiphiness) - Working on the [Identity DAO](https://github.com/dorgtech/id-dao) project's GoodDollar dApp integration.
- [Zak](https://github.com/zakhap) - Blessing the [Identity DAO](https://github.com/dorgtech/id-dao) project with his design and project management skills.
- [Hector](https://github.com/mrrobot16) - Working on adding additional, highly requested, features to the [DAOcreator](https://github.com/dorgtech/DAOcreator).
- [Cesar](https://github.com/cbrzn) - Working on adding additional, highly requested, features to the [DAOcreator](https://github.com/dorgtech/DAOcreator).
- [Eric](https://github.com/arsena21) - Developing a product specification & a go to market roadmap for the Ideologi project.
- [James](https://github.com/Flash-Git) - Working on the Nectar DAO front-end.

## Veriledger Takes On dOrg's Accounting

dOrg has engaged [Veriledger](https://veriledger.io) to take on accounting solutions for legal DAOs. This includes:

- Tax reporting templates for DAO participants
- Financial statements for DAOs
- Automated bookkeeping processes for DAOs
- Tax strategies for DAOs

Like our [previous engagement with Gravel & Shea](https://www.gravelshea.com/2019/06/dorg-launches-first-limited-liability-dao/) to develop legal solutions for DAOs, we hope that this engagement will yield solutions that further reduce the frictions between legacy systems and DAOs while bringing more attention to the ecosystem. See Veriledger's previous work on the topic [here](https://medium.com/veriledger/dao-accounting-dc496e6fb57f).

## Helping other Dev Shops build on DAOstack

In addition to growing itself, dOrg has also helped on-board and advise new developer teams in the ecosystem:

- [_prtcl](https://github.com/uprtcl/spec): Helping Pepo & Gillem specify their Alchemy integration.
- [Ape Unit](https://apeunit.com/): Helping to walk them through the DAOstack architecture and scope a project.
- [AliceDapp](https://www.alicedapp.com/): Helping Mark redesign Alchemy mobile.
- [Odyssy](https://odyssy.io/): Discussing the possibility of adding DAOstack support to their Moloch DAOcreator.
- [Level K](https://www.levelk.io/): Collaborating with us on the U.I. for the DAO bonding curve project.

# Self-Sustainability

## Gnosis: Bonding Curves for DAOs

Bonding curve support for DAOs to allow continuous funding.

### Present

- A new dividend model that is highly scalable and fully on-chain was developed and integrated.
- The alchemy integration is underway.
- BC-DAPP, the continuation of this project for use by the dxDAO, has been scoped out and proposed to the dxDAO.

### Future

- Development of BC-DAPP
- Improved alchemy integration with custom views
- Third-party auditing

## GoodDollar: Identity DAO

DAO-curated registry of human identities to be integrated with the GoodDollar app.

### Present

- [Contracts](https://github.com/dOrgTech/ID-DAO/tree/master/dao) Finished
- [Client Library](https://github.com/dOrgTech/ID-DAO/tree/master/client) 90% complete
- Gooddollar dApp & Server integration 80% complete

### Future

- Gooddollar dApp polish
- Alchemy views integration