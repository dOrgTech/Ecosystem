# RFC-09: DAOcomponents

## User Story

As a small team developing a widely used protocol (DeversiFi, Bancor, Orchid, Totle, Compound), I am considering to use DAOstack to transition protocol governance to users and major stakeholders.

As the administrator of a large hackathon, meetup, or events community (Odyssey, ETHGlobal, FestDAO, Crypto Mondays, Bitcoin Malaysia, 1 Mil Devs), I am considering to use DAOstack to transition community governance to members.

I want my users to interact with the DAO from within my website or app instead of sending them to Alchemy so that I control the end-to-end user experience.

### Current
Use the [Client library](https://github.com/daostack/client) directly. With this approach there is a large learning curve, and it's not obvious how to integrate the library with a React application.

The library does complex asynchronous actions, and handling that elegantly within your React applications is additional work that each application will have to do on their own.

Additionally the application will have to do additional work to reduce boilerplate code, as different sub pieces of the UI will need a shared context (Members, Proposals, etc).

### New

With DAOcomponents, I can DAO-enable my React app by adding just 2 components. The library seamlessly handles all loading, error handling, re-rendering, or boilerplate for me under the hood.

## Impact on Adoption

- Horizontally scale the stack by making it an order of magnitude easier to interact with from other front-ends.

- Generate buzz & attract major crypto protocols to use DAOstack by showing how they can integrate it into their existing front-ends with a few lines of code.

## Roadmap

| Time | Workload | Description |
|-|-|-|
| 2 weeks | 1.0 FT | Update for client 2.0 |
| 3 weeks | 1.0 FT | Demo App + Documentation |

## Detailed Design

Here's a short tutorial that shows how simple this is:

1. Add DAOcomponents to your React project...  
`npm i --save daocomponents`

2. Connect to the Arc protocol + your DAO...  
    `App.jsx`
    ```html
    <Arc config={mainNetConfig}>
      <DAO address="0xMY_DAO">
        <SomeOtherComponent />
      </DAO>
    </Arc>
    ```

3. Now, we can read and write to our DAO in any part of application. For example, we may want to show a list of all members in:  
    `SomeOtherComponent.jsx`
    ```html
    <Members>
      <Member.Data>
      {(member: MemberData) => (
        <>
          <div>Address: {member.address}</div>
          <div>Reputation: {member.reputation}</div>
        </>
      )}
      </Member.Data>
    </Members>
    ```

See [here](https://github.com/dOrgTech/DAOcomponents/blob/master/README.md) for more tutorials on how to use the library.

## Open Questions

None.
