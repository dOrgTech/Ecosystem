# RFC-06: ENS Manager

## User Story

### Current

User must navigate between `EthRegistrar`, `EnsRegistry` and `EnsPublicResolver` plug-ins to call individual functions on respective ENS contracts. There is no place in Alchemy to view the DAO's ENS Names.

ENS Names don't render in the Member List or Proposals.

### New 

User enters "ENS Dashboard", where they can manage all domains owned by the DAO. Editing or adding any new domains will trigger a proposal on the respective ENS contract.

If the ENS Dashboard is not added, there will be a button on this section that will create all 3 plug-in manager proposals.

Throughout the UI, ENS Names render properly.

## Impact on Adoption

This would significantly improve DAOstack's interoporability with the web3 ecosystem which is increasingly utilizing ENS.

## Roadmap

| Time | Workload | Description | 
|-|-|-|
| 1 week | 1.0 FT | Dashboard UI - Design |
| 2 weeks | 1.0 FT | Dashboard UI - Implementation |
| 2 weeks | 1.0 FT | Registration/Update Functionality + Interacting with ENS Contracts |

## Detailed Design

1. Dashboard UI - new section accessible through side bar for viewing and managing ENS domains

	- Table with registered ENS Names

	- Each entry has "edit" button that triggers a modal with basic options like set resolver or content hash. Advanced tab shows all possible actions.

	- Button to register a new ENS Name

2. Registration/Update Functionality: Actions in the dashboard generate proposals in the respective plug-in.

3. Reading from ENS Contracts

	- ENS Name Resolution: Allow proposal recipients to be ENS Names

	- Reverse Resolution: Display ENS Name wherever addresses are displayed (DAO members or proposal)

## Open Questions

None
