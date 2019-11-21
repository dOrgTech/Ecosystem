*An overview of dOrg's progress in the 2nd month (Nov 1 - 30) of our six month engagement with Genesis DAO.*

*For context, [see the recurring proposal here](Genesis_Recurring_Funding.md).*

# DAOcreator

- **Automated Alchemy Support** is here! Newly deployed DAOs will automatically show up in Alchemy if you visit their URL.

- **Improvements & Bug Fixes**

	- [Various deployment improvements](https://github.com/dOrgTech/DAOcreator/pull/238)

		- Detect unsupported networks

		- Detect no web3 support
		
		- Add alert before window close during migration

		- Properly display errors in the migration log

	- [Remove whitespace from CSV import](https://github.com/dOrgTech/DAOcreator/pull/217)

	- [Ensure Rep and Token of founder not set to 0](https://github.com/dOrgTech/DAOcreator/pull/231)

	- [Fix leading 0 bug](https://github.com/dOrgTech/DAOcreator/pull/226)

	- [Fix time validation bug](https://github.com/dOrgTech/DAOcreator/pull/227)

	- Save DAO config in local storage & [preview config before resume](https://github.com/dOrgTech/DAOcreator/issues/232)

	- [Upgrade arcVersion dependency](https://github.com/dOrgTech/DAOcreator/pull/235)


- **DAOcreator Redesign** interactive wireframe & intensive community feedback

	- Play with [interactive wireframe here](https://www.figma.com/proto/t77rlBAupEeqIYHFBBpqrl/Playground?node-id=98%3A1072&viewport=213%2C267%2C0.1505504995584488&scaling=min-zoom)

	<img src="../img/beta01.png" width="800">

	- Community feedback: focus group with DAOstack core, [DAOtalk forum post](https://daotalk.org/t/daocreator-redesign-feedback-round-1/993), [feedback form](https://dorgtech.typeform.com/to/RjMhEq), and [open call for one-on-ones](https://calendly.com/orishim/daocreator)


### Next Steps

- Continue conducting user research to iterate on wireframe, develop into full mock-up, begin implementing front-end.

- Get newly deployed DAOs on Alchemy front-page. [Solution proposed here](https://github.com/daostack/alchemy/issues/1246).

# Use Cases & Integration

- **[Gasless Rep Redeem]([solution](https://github.com/dOrgTech/TxPayerService))**:

	- Dynamic handling of insufficient balance and gas limits

	- Migrated from Heroku to Netlify to run as serverless function

	- Testing and gathering feedback from DAOstack core (Jelle, Oren, Eylon)

- **_prtcl Alchemy Integration**: Worked on [wiki componentent](https://github.com/dOrgTech/js-uprtcl/tree/wiki_component_creation)

- **[Auto-Generated Proposals from Alchemy URL](https://github.com/daostack/alchemy/pull/1226)**: Add the ability to open a proposal template for a user via embedding its pre-filled-out contents within the URL's parameters. Read more about the rationale [here](https://github.com/daostack/alchemy/issues/1181).

### Next Steps

- Begin working on new tooling to enable dHack ETH Denver 

- Finish testing and ship Gasless Rep Redeem

- Continue to assist in the uprtcl integration

# Ecosystem

- Continued to specify good first time and advanced issues for new OS contrubtors to DAOstack in a follow-up session with Kate, Shiv and others.

- Presented on DAOstack, dOrg and the DAOcreator tool at Jason's event in Bangkok

TODO ADD OTHERS

### Next Steps

TODO

# DAO Admin

TODO

### Next Steps

TODO