# RFC-15: 3box Comments

## User Story

### Current
Currently we can discuss inside proposals using a centralized solution like Disqus. However it does not have the nature of chat, rather its just like a forum board.

### New 
We want a decentralized messaging component inside proposals.

As a User I want to be able to chat inside my proposals, so that we can start discussions and answer questions related to proposals.

As a User I want to see a list of messages.

As a User I want to send messages.

## Detailed Design

Based of 3box documentation https://docs.3box.io/build/web-apps/messaging/persistent-threads

We are gonna use persistent threads for our messages.

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
| 1 week | 0.25 FT | Steps 1-3 
| 1 week | 0.25 FT | Steps 4-6 
| 1 week | 0.25 FT | Steps 7-9

## Open Questions

- Do we want the ability to update and delete messages?

- There is feature to add moderators do we want that as well?

## Impact on Adoption

Adding the ability to chat will enable us to discuss in real time proposals and increase collaboration among the community. 