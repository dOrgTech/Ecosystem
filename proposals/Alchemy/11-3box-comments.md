# RFC-15: 3box Comments

## User Story

### Current
Currently a user needs a 3box for an Alchemy profile but a Disqus account to comment on proposals.

### New 
As a User I want to comment on proposals without creating Disqus account, so that we can fluidly start discussions related to proposals.

As a User I want to be able ot see and post messages.

## Detailed Design

Based of 3box documentation https://docs.3box.io/build/web-apps/messaging/persistent-threads

We are going to use persistent threads for our messages.

### Steps to take

1. Configure "3box threads" on alchemy.

2. Authenticate to a 3box space where a thread is stored in order to perform operations such as creating a thread, joining a thread, posting messages, removing messages

3. Add ability to create new threads

4. Add ability to join a thread.

5. Add ability to view messages of a thread.

6. Add ability to post messages on a thread.

7. Add ability to delete message.

8. Add the ability to send messages to one specific proposal.

9. List messages that belong to each proposals.

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 1 week | 0.25 FT | Steps 1-3 |
| 1 week | 0.25 FT | Steps 4-6 |
| 1 week | 0.25 FT | Steps 7-9 |

## Open Questions

- Do we want the ability to update and delete messages?

- Do we want to include the DAO Wall? (DAO forum unrelated to particular proposals)

- There is a feature to add moderators. Do we want that as well?

## Impact on Adoption

Adding a decentralized messaging component inside proposals will reduce user frictions and increase user engagement. It will make the whole app a more integrated experience without reliance on centralized third-parties.


