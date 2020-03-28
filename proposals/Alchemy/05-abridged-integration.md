# RFC-05: Abridged Integration

## User Story

### Current
If a new user wants to interact with Alchemy, they needs to download a browser extension in order to be able to log in into the dApp and also needs to buy ether if they wants to create a proposal/stake/vote.

### New 
As a new user I want to login with my email and password. I will not be required to download any additional browser extensions to interact with the blockchain. I will also be able to buy crypto with my fiat money (credit / debit cards).

## Impact on Adoption

This will lower the bar for new user onboarding dramatically, as it will be similar to a traditional web2 application's onboarding process. More details on this way of thinking about web3 onboarding can be found here: https://medium.com/abridged-io/layer-2-first-developer-flow-the-first-2-minutes-217c2bfd5868

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 4 weeks | 1.0 FT | Create the actions for login/sign up, for this actions we are going to create a class to manage the auth methods to allow the user web3 attributes (address) to interact with alchemy functionalities |
| 1 week | 1.0 FT | Implement Crypto On-Ramps with Ramp Instant |

## Detailed Design

- Create views for traditional auth - Register and Login
  - We are going to modify the web3reducer to handle the "traditional users", creating a new enum which is going to be `userType`, this way can differentiate how the did the user authenticate into the application; and a method 
  - When the user signs up, we are going to initialize [Archanova SDK](https://github.com/netgum/archanova/blob/develop/docs/sdk/configuration.md) to store user credentials on the database.
  - When the user logs in for the first time, a unique ENS Label is going to be generated, and a new account is going to be created; after that, a device will be connected to the account (which is the device where the user is logging in). At last, a encrypted key store is going to be generated and saved into the db, so when the user logs in again, we pass it to the initialization of the SDK and they can get back is account. NOTE: If user loses his password they can not take his account back.
  - Implement the [`submitAccountTransaction`](https://playground.archanova.run/#send_account_transaction) method from the sdk so the user can vote/stake/propose.

- Create a "Buy crypto" module for web2 (traditional users), so they can pay for gas tx; here the user can pay for ETH with fiat
  - We are going to use [Ramp instant SDK](https://instant.ramp.network/) to allow new users to buy ether with USD or EUR.

This is an example app with abridged integration: https://github.com/odyssy-automaton/moloch-pokemol

## Open Questions

None