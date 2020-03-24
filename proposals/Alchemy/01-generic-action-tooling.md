# RFC-01: Generic Actions Tooling

Alchemy was built to provide a generic way for interacting with DAOs. With that, Alchemy requires information from the user who needs to have a high degree of knowhow of the Daostack framework and the on-chain application the DAO wants to connect with. This leads to a huge barrier for any user, even developers need to look into how exactly the ENS contracts work.

## User Story

### Current

User wants to add ENS support to an already existing DAO with 100 members. User goes to the internal DAO interface on Alchemy with the goal to achieve his goal. Looking through the cards, he/she gets confused about the technical words like "Funding and voting power" or "Scheme Manager". The user is asking himself what are schemes, which leads to even more confusion. "Scheme Manager" indicates clearly that something can be managed so the user clicks on the Scheme Manager. User clicks on New scheme proposal, to explore what Scheme Manager is all about, a modal pops up with three main categories "Add Plugin, Edit Plugin and remove Plugin". User is confused as he believe he would add a new scheme and now the interface is showing with the term "Plugin". User wont know what to do and since the actual alchemy UI is not intuitive, adding ENS support wont be an easy task.

In resume:

Adding GA plugins within Alchemy currently has the following problems:  
- No UI for configuring & deploying a new GA plugin contract – must be done by a skilled programmer.
- No UI for knowing what types of GAs Alchemy supports (ENS Registrar, Uniswap, etc).
- No UI for creating new types of GAs that Alchemy can support (Compound, etc) – must be PR'd into Alchemy for them to be usable.
- Complex UI for adding a GA plugin to the DAO via the plugin manager.
- Subgraph does not pickup on newly deployed GA plugin contracts.

When an user wants to add the Generic Scheme into it's DAO, he needs to look for the Generic Scheme address, create a proposal in the Scheme Registrar and create a PR in the subgraph to use the new scheme

### New

- As an excited DAO member I want to easily extend the functionality of my DAO, so that I can focus on using the DAO to achieve its goal. Going to the main alchemy interface of my DAO, I see a card called "Manage Connections" with a small description "Manage connection to contracts/applications" which signals me that I could maybe add a connection to the ENS application/contract. Clicking on the card leads me to a view with all active connections my DAO currently has. I have the option to add, remove or edit a connection so I go with add a connection. I see a modal which presents me with popular connections like the ENS system or Uniswap. I click on the ENS system which leads me to a view which is all about the ENS system connection. I can observe how many DAOs have a connection with it which gives me confidence that this is the right connection I want to make. A big blue button with the description "Add ENS connection" clearly indicates me that this will lead me to my end goal. I click on the blue button and metamask is popping up to sign the transaction. Alchemy detects my transaction signing and while I am waiting for the transaction to be confirmed alchemy shows me tipps of how I can be more efficient with my DAO. After the transaction got confirmed, I see a pending connection in my connection overview. I click on the pending connection item which collapse and indicates me that my recent metamask transaction triggered three proposals for the main ENS contract, the .eth registry and the public resolver. While I didn't knew that it was required to have three connections to a specific contract, alchemy made the process incredible easy by doing the heavy lifting for me.

- As a protocol developer, I want to give DAOstack DAOs the ability to interact with my smart contracts (ENS, Uniswap, Compound), so that adoption of my protocol increases.

This is going to be splitted in two parts, which are: 
  - The creation of a Generic Scheme through UI
  - A marketplace of plugins (Generic schemes) in alchemy, so the user can add existing generic schemes into his DAO by just clicking a button

## Impact on Adoption

The ability to easily call existing smart contracts is crucial for adoption by any Ethereum projects interested in DAOifying their governance with DAOstack.

Many projects are currently choosing to use Aragon specifically because [Aragon Agent](https://aragon.org/agent/) makes it easy to interface their DAO with smart contracts.

This is a HUGE missed opportunity right now.

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 3 week | 1.0 FT | Part one .1: Create UI of the three forms that will allow any user to create a new generic scheme |
| 2 week | 1.0 FT | Part one .2: Create `GA Factory` contract to access created GS created through UI |
| 3 week | 1.0 FT | Part two: Create a new section to show the generic schemes that has been added through the `GA JSON files` and `GA Factory`, also allow the user to create a new proposal in the DAO's Scheme Manager |

## Detailed Design

### Terminology

**GA Creator**: UI for configuring & deploying new generic action plugins from within Alchemy. Deployment via the UI will (1) deploy a new GA plugin contract via the ***GA Factory*** and (2) call create a proposal in the DAO's Plugin Manager to add the new GA plugin.  
**GA Factory**: Contract factory that spawns new GA plugin contracts. This is needed until Arc-Hives is live.  
**GA Designer**: UI for defining new generic actions (Compound, Uniswap, Moloch, etc). The UI will be a front-end for defining [GA JSON files](https://github.com/daostack/alchemy/tree/dev/src/genericSchemeRegistry/schemes), and proposing them to the ***GA Registry***.  
**GA Registry**: On-chain registry of GA JSONs. This registry should be managed by a DAO made up by the stake-holders of Alchemy. The Alchemy DAO.  
**Known GA**: A Generic Action that's registered in the registry.  

### Steps to take

Part one (`GA Creator`):
  - Create `GA Factory` (contract) to allow generic schemes to be showed as `Known GA`
  - Create a new section called `Create new plugin` on UI, this will be separated into three steps (forms) which are going to be:
    - A form for that will allow the user to set up voting configuration paremeters for new scheme
    - User can define which methods (and parameters) the new generic scheme will have, this is the `GA Designer`
    - Set address of contract to call
    - When the users clicks `Submit` a call to the `GA Factory` will be triggered, so the new scheme is added, and then a new proposal in the scheme registrar of the DAO where the Generic Scheme is being added, is going to be created to add this new scheme
 
Part two:
  - Develop a new section called "Manage connections". Here members of a DAO can add existing Generic schemes that has been added into `GA JSON files` and the `GA Factory`. Users will see the existing generic schemes been with just one click, they will create a proposal in the scheme registrar so they can add any generic scheme that's showed in this section.

## Open Questions

- How will this feature be affected by Stack 2.0 changes?

- Would it be better to focus on creating a "generic generic action" rather than encouraging a proliferation of particular generic actions?
