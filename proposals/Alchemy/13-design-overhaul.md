# RFC-13: Design Overhaul

## User Story

### Current

-   Protocol-centric (built around DAO's capabilities), not user-centric (built around user experience)

-   No onboarding flow

-   UI is overly complex, confusing and leaves much heavy lifting to the user.

    -   User manually "follows" DAOs

    -   User must navigate plug-in menu to find active proposals

    -   Sidebar is overwhelming

    -   Proposal detail & new proposal views are overwhelming

### New

As a new user I want to quickly create a new DAO or join an existing DAO.

As a DAO member I want to see a compact overview of the finances +
recent activity in all my DAO(s).

As a DAO member I want to quickly vote, stake, create and redeem proposals in my
DAO(s).

As an advanced user I want to edit my DAO's configuration.

## Impact on Adoption

Attract and retain new users, especially since most existing DAO UIs (alchemy, aragon, moloch, colony) are incredibly complicated for new users. We could attract more crypto players in addition to crypto newbies.

Increase user engagement in existing DAOs -> increase effectiveness of DAOs.

## Roadmap

| Time | Workload | Description |
|-|-|-|
| 4 Weeks | 1.0 FT | (Mock-up + feedback + iterate) x 3 |
| 4 Weeks | 2.25 FT | Implement `Home` + `Featured` + `DAO Summary Card` views (2.0) + continued design improvement (0.25) |
| 6 Weeks | 2.0 FT | Implement `Proposal Feed`, `Proposal Details`, `Create Proposal`, `Members`, `Settings` views |

## Detailed Design

Redesign user flow to be simple by default, with advanced features/info hidden unless user chooses to expose them.

### Views

#### Home

-   Detect if user is in DAO(s)

    -   If no, display "Create new DAO" or "Explore featured DAOs" buttons

    -   If yes, show user her DAO summary card(s)

#### DAOs

-   **Featured**: List of DAO Summary Cards for most active DAOs

-   **DAO Summary Card**

      -   Current treasury

      -   Recent payments in/out

      -   Recent proposals passed/failed

      -   Active proposals

#### DAO

-   **Proposal Feed**: One view that aggregates proposals from all different categories

    -   Defaults to showing active proposals: boosted, pending, regular

    -   Can also filter proposals by: categories (AKA plug-ins/schemes) and status (active, passed, failed)

-   **Proposal Details**: See details about an individual proposal

-   **Create Proposal**: Create new proposal

    -   Choose category from dropdown

    -   Hide all optional fields (only show if the user checks them)

- **Members**: Member list

- **Settings**: advanced view for viewing and proposing changes to plug-ins

## Open Questions

None
