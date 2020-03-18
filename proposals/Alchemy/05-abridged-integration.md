# RFC-05: Abridged Integration

## User Story

### Current
If a new user wants to interact with Alchemy, he needs to download a browser extension in order to be able to log in into the dApp and also needs to buy ether if he wants to create a proposal/stake/vote.

### New 
As a new user I want to login with my email and password, and access to the blockchain, so I don't need to complicate downloading browser extensions that I do not know how to use and also I want to buy Ether with my fiat money.

## Detailed Design

- Create views for traditional auth - Register and Login
  - We are going to modify the web3reducer to handle the "traditional users", creating a new enum which is going to be `userType`, this way can differentiate how the did the user authenticate into the application; and a method 
  - When the user signs up, we are going to initialize [Archanova SDK](https://github.com/netgum/archanova/blob/develop/docs/sdk/configuration.md) to store user credentials on the database.
  - When the user logs in for the first time, an unique ENS Label is going to be generated, and a new account is going to be created; after that, a device will be connected to the account (which is the device where the user is logging in). At last, a encrypted key store is going to be generated so when the user logs in again, we pass it to the initialization of the SDK and he can get back is account. NOTE: If user loses his password he can not take his account back.
  - Implement the [`submitAccountTransaction`](https://playground.archanova.run/#send_account_transaction) method from the sdk so the user can vote/stake/propose.

- Create a "Buy crypto" module for web2 (traditional users), so they can pay for gas tx; here the user can pay for ETH with fiat
  - TODO... (What should we use? Wyre or Moonpay)

This is an example app with abridged integration: https://github.com/odyssy-automaton/moloch-pokemol


## Roadmap

| Time | Workload | Description | 
|-|-|-|
| To be defined | 1.0 FT | Create the actions for login/sign up, we can use PostgreSQL or Amazon Incognito (still need to be defined), for this actions we are going to create a class to manage the auth methods to allow the user web3 attributes (address) to interact with alchemy functionalities |
| To be defined | 1.0 FT | Implement Crypto On-Ramps |


## Open Questions

Should we use AWS Incognito or PostgreSQL db?

My personal opinion is that alchemy already has a database and a server so we can make use of it, it will save us time and it's easier to develop.

## Impact on Adoption

This will helps the on boarding of new users into the dApp, since it's going to work as a traditional web2 app (Logging in with email and password).
More details on the impact can be found here: https://medium.com/abridged-io/layer-2-first-developer-flow-the-first-2-minutes-217c2bfd5868