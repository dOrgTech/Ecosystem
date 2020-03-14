# RFC-02: Voting configuration editor

## User Story

### Current
Editing a DAO plugin's voting machine configuration is currently super complicated. Users do not have an easy to use interface within Alchemy for doing this. Currently, a user must:

- Instantiate the Genesis Protocol contract through an external source (Remix or CMD with web3 lib)
- Add the params hash manually, which can cause problems because the parameters need to be validated (sent in certain order, max-min values); and this will make the tx fail
- Instantiate the scheme that we want to modify and call the method [setParameters](https://github.com/daostack/arc/blob/master/contracts/universalSchemes/ContributionReward.sol#L99) 

### New
As a non technical user of the DAO I want to manage and set up my organization in any way that I want to, this way, if me as founder, do something wrong at the time of the creation of the the DAO or eventually me and my group just want to change the rules of a scheme of the organization, we will be able to do it through an UI, making it easier to add a new voting configuration for the desired scheme.

## Detailed Design

We want to modify the existing "plugin information" view to allow for users to make edits to the genesis protocol form, and "save" those changes to their DAO. This will prompt the users with 2 transactions:

- Add the parameters to the voting machine (Genesis protocol contract instance).
- Add the parameters to the scheme.
- Create a proposal on Plugin Manager to edit the plugin being modified.

We need to do this with every scheme, one by one, we are going to start with the universal ones (Funding and Voting Power, Plugin Manager and Blockchain Interaction).


## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 2 weeks | 1.0 FT | Edit client library to create the instance of the Genesis Protocol contract with the address that's associated with a selected DAO, then we will create two transactions, one to create the hash of the parameters of the voting machine and the second one to add this hash into the desired scheme |
| 1 week | 1.0 FT | Here we are going to edit alchemy UI, we are going to add an `Edit` button on the top right of the plugin information view (and will only appear if the DAO has the Plugin Manager), and it will have a form with the voting machine params (this will use the library `@dorgtech/daocreator-lib` for validations), when the user clicks submit, generate the two tx and then the proposal on the plugin manager  |

## Open Questions

None
