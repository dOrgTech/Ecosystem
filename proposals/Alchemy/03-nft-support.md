# RFC-03: NFT Support

## User Story

### Current
Alchemy currently lacks the ability to display, transfer and create NFTs (ERC721s and ERC1151).

### New 
As an artist, I want to collaborate with other artists and create/sell NFT art on OpenSea (to share profit) with a storefront or through bundling.   
As an organisation, I want to award NFTs (badges/awards).   
As a user, I want to be able to see what NFTs a DAO owns and use them to create a revenue model.  

## Detailed Design

This proposal outlines how with the addition of 2 new generic schemes, users will be able to add NFT functionality to their DAOs.

#### 1. NFT Support Scheme

##### Functionality
- Gives DAOs the ability to transfer NFTs (whitelisted NFTs are selectable from drop-down, with optional manual override for unwhitelisted tokens)
- Gives DAOs the ability to list owned tokens for sale on OpenSea and accept existing orders (in Eth or ERC20s)
- Gives DAOs the ability to whitelist NFTs (The front end will be aware of whitelisted NFTs)

##### Architecture
- The NFT Support generic scheme needs to be created
- The NFT view needs to be created to show owned NFTs
    - Query metadata (image, name, sale status, owned status, etc...)
    - Updates on whitelisted NFT transfers
    - Custom views for special NFTs (eg. ENS)
- The NFT Support proposal forms need to be created
    - Whitelisting
    - Transfering
    - Sale listing
    - Offer handling
    - Updating metadata (for DAO owned NFTs)
    

#### 2. NFT Creation Scheme:

##### Functionality
- Gives DAOs the ability to deploy new NFT Contracts
- Gives DAOs the ability to create new NFTs from these contracts
    - The created NFTs can be transfered
    - The created NFTs can be listed for sale on OpenSea (in Eth or ERC20s)
    - The created NFTs can have their metadata updated

##### Architecture
- The NFT Creation generic scheme needs to be created
- The generic NFT contracts that will be deployed by this scheme need to be created
- The Created NFT view needs to be created to show created NFT contracts
    - Query metadata (image, name, count, etc...)
- The NFT creation proposal forms need to be created
    - Deploying new NFT contracts
    - Minting new NFTs from existing NFT contracts
    - Sale handling
    - Offer handling
    - Updating metadata 

## Roadmap
| Time | Workload | Description | 
|-|-|-|
| TODO | 1.0 FT | NFT Support Scheme |
| TODO | 1.0 FT | NFT Creation Scheme |

## Questions
- Which token standards should be supported?
- Are there "super" NFT contracts where single contract addresses are used for multiple NFTs.
- Are there many NFTs that fail to follow the token standards?
- Where will created NFT metadata be stored?
- Which contract model should be used for the NFT Creation Scheme (NFT specific contract, DAO specific NFT contract, or a super generic NFT contract used by all DAOs)

## Impact on Adoption
This would allow large brands to run promos using DAOs that issue NFTs. It could also serve as a bridge to on-board the large community of NFT enthusiasts / artists on platforms such as OpenSea.
