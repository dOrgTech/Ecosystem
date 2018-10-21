# Key Scenarios  
This is a high level, technology independent look at the scenarios we're interested in enabling.  

### Feature Groups  
[Legal]  
[Finance]  
[Community]  
[Development]  
[Project Management]  
[*] == all groups above  

|  # | Scenario | Feature Group(s) |  
| -- | -------- | ---------------- |  
|  0 | [scenario spec template](./scenario-specs/0-spec-template.md) | |  
|  1 | [dOrg Setup and Configuration](./scenario-specs/1-setup-and-configure.md) | [*] |  
|  2 | Public dOrg Visibility | [*] |  
|  3 | Private dOrg Visibility | [*] |  
|  4 | Open dOrg Participation | [*] |  
|  5 | Closed dOrg Participation | [*] |  
|  6 | Browse a dOrg | [Community] |  
|  7 | dOrgs Are Discoverable | [Community] |  
|  8 | User Profiles | [Community] |  
|  9 | Support Attested Users | [Legal]<br>[Community] |  
| 10 | Support Anon Users | [Legal]<br>[Community] |  
| 11 | Instant Communication | [Community]<br>[Project Management] |  
| 12 | Structured Communication | [Community]<br>[Project Management] |  
| 13 | Add Member / Contributors to dOrg | [Community]<br>[Project Management] |  
| 14 | Task Creation | [Project Management] |  
| 15 | Task Rewards | [Project Management] |  
| 16 | Consensus Functionality and Applicability | [Project Management] |  
| 17 | Task Prioritization, Grouping, and Dependencies | [Project Management] |  
| 18 | Repository Connections | [Development]<br>[Project Management] |  
| 19 | Automated Deployments | [*] |  
| 20 | Funding / Investing | [Finance] |  
| 21 | Enable Verifiable Revenue Streams | [Legal]<br>[Finance] |  
| 22 | Legal Agreements | [Legal] |  

---
## Public dOrg Visibility  
* Anybody can browse the dOrg.  

---
## Private dOrg Visibility  
* Only invited members can browse the dOrg.  

----
## Open dOrg Participation  
* Anybody can participate.  

---
## Closed dOrg Participation  
* Only invited/accepted members can participate.  

---
## Browse a dOrg  
* See activity.  
* See sub-communities.  
* Only if it isn't a private visibility dOrg.  

---
## dOrgs Are Discoverable  
*Users considered: investors, skilled professionals, community members / enthusiasts, dOrg's looking for collaborators (other dOrgs or individuals).*  
* Search for a dOrgs (togglable discoverability).  
  * ex: Search for a dOrg of graphic designers.  
  * Search using our dApp, or find a dOrg through a search engine (support SEO).  
* Search for "help wanted" postings from dOrgs.  
  * ex: Front-end engineer looking for work.  
* Allow dOrgs to post to a global feed, similar to twitter.  
  * ex: dOrg "Foo" has a new release and wants to post a video explaining it.  

---
## User Profiles  
* Reputation  
* Activity Feed  
* Memberships  
* Configurable profile information  
* Link to other profiles  

---
## Support Attested Users  
* Support attestation networks that tie on-chain accounts back to individuals in the real world.
  * This is needed to correlate people's actions for legal purposes.  

---
## Support Anon Users  
* Support users as anonymous individuals with only an on-chain identity.
  * These users would have limited abilities within the dOrg (can't sign legal documents that are indented to be enforced off-chain).  

---
## Instant Communication  
* dOrg chat.  
  * Members within a dOrg can create channels or private messages.  
* Community chat.  
  * Cross dOrg channels and private messages.

---
## Structured Communication  
* dOrg forums.  
  * Members within a dOrg can create forum threads.
  * Similar to GitHub tasks.  
* Community forums.  

---
## Add Member / Contributors to dOrg  
* It should be possible to add members / contributors to a dOrg.  

---
## Task Creation  
* It should be possible to create tasks that's done in the dOrg.  

---
## Task Rewards  
* It should be possile to add rewards to tasks.  

---
## Consensus Functionality and Applicability  
* Support configurable consensus functionality.  
  * ex: 2/3 is required to form consensus.  
  * ex: Only top 50% rep users can vote.  
  * ex: Any attested user, regardless of rep, can have 1 vote (great for social impacting dOrgs that want to have the people have a say).  
* Support configurable consensus applicability.  
  * ex: Require consensus for task creation.  
  * ex: Require consensus for reward assignment.  
  * ex: Require consensus for adding new members.  
  * ex: Require consensus for publishing new builds.  

## Task Prioritization, Grouping, and Dependencies  
* Task `A` must be completed before task `B`, it has top priority of all other tasks in `Milestone 1`.  
  * Prioritization: 0-100  
  * Grouping: Milestones  
  * Dependencies: Protocol-enforced order of completion  

## Repository Connections  
* It should be possible to connect repositories to a dOrg (Public and Private).  
  * ex: GitHub repository  
  * ex: GitHub organization  
  * ex: BitBucket  

## Automated Deployments  
* It should be possible to deploy the software created in an automatic and decentralized way.  
  * ex: Build and publish app to store.  
  * ex: Push new build of web app.  
  * ex: Upload freshly built binaries to a repository.  

## Funding / Investing  
* It should be possible for a project to accept funding if they want.  
  * Sell utility tokens.  
  * Sell dividend tokens.  
  * Sell security tokens.  
  * Accept donations.  
  * Accept funding for specific tasks (bounties).  

## Enable Verifiable Revenue Streams  
* It should be possible to verify the revenue stream is streaming through a particular smart contract.  
  * Ensures the dividend token holders are being compensated appropriately.  
  * Enables analytics.  
  * This could be solved using a combination of standard smart contracts, automated code scanning, community auditing, and tradition legal agreements.  

## Legal Agreements  
* There should be a way of adding legal agreements to a dOrg (and signing them) in a compliant way.  
  * These contracts could facilitate:  
    * dOrg as corporate entities (better liability insulation).  
    * Agreements between individuals and between dOrgs for anything that should have a legal recourse if things go wrong.  