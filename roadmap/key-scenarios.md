# Key Scenarios  
This is a high level, technology independent look at the scenarios we're interested in enabling.  

### Feature Groups  
[Legal]  
[Finance]  
[Community]  
[Development]  
[Project Management]  
[*] == all groups above

| Scenario | Feature Group(s) | Implementation Spec |  
| -------- | ---------------- | ------------------- |  
| [dOrg Setup and Configuration](#dorg-setup-and-configuration) | [*] | TODO |  
| [Public dOrg Visibility](#public-dorg-visibility) | [*] | TODO |  
| [Private dOrg Visibility](#private-dorg-visibility) | [*] | TODO |  
| [Open dOrg Participation](#open-dorg-participation) | [*] | TODO |  
| [Closed dOrg Participation](#closed-dorg-participation) | [*] | TODO |  
| [Browse a dOrg](#browse-a-dorg) | [Community] | TODO |  
| [dOrgs Are Discoverable](#dorgs-are-discoverable) | [Community] | TODO |  
| [User Profiles](#user-profiles) | [Community] | TODO |  
| [Support Attested Users](#support-attested-users) | [Legal]<br>[Community] | TODO |  
| [Support Anon Users](#support-anon-users) | [Legal]<br>[Community] | TODO |  
| [Instant Communication](#instant-communication) | [Community]<br>[Project Management] | TODO |  
| [Structured Communication](#structured-communication) | [Community]<br>[Project Management] | TODO |  
| [Add Member / Contributors to dOrg](#add-member-/-contributors-to-dorg) | [Community]<br>[Project Management] | TODO |  
| [Task Creation](#task-creation) | [Project Management] | TODO |  
| [Task Rewards](#task-rewards) | [Project Management] | TODO |  
| [Consensus Functionality and Applicability](#consensus-functionality-and-applicability) | [Project Management] | TODO |  
| [Task Prioritization, Grouping, and Dependencies](#task-prioritization-grouping-and-dependencies) | [Project Management] | TODO |  
| [Repository Connections](#repository-connections) | [Development]<br>[Project Management] | TODO |  
| [Automated Deployments](#automated-deployments) | [*] | TODO |  
| [Funding / Investing](#funding-/-investing) | [Finance] | TODO |  
| [Enable Verifiable Revenue Streams](#enable-verifiable-revenue-streams) | [Legal]<br>[Finance] | TODO |  
| [Legal Agreements](#legal-agreements) | [Legal] | TODO |  

---
## dOrg Setup and Configuration  
* Setup a dOrg from scratch.  
  * Support the importing of a dOrg from other services like GitHub, LinkedIn, etc, helping hasten migrations.  
* Configure a dOrg.  
  * Setup the rules by which the dOrg operates.  
* Reconfiguration rules.  
  * Make rules on how a dOrg could reconfigure itself.  
    * Immutable.  
    * Top 10% of rep holders required.  

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