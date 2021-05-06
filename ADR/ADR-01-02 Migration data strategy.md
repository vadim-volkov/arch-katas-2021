ADR-01-02 Migration data strategy

# Satus
Proposed

# Context

We have a lot of customer, subscription, billing and other information in current databases. We need to make sure that all information will be available in new solution, and minimize data migration time.

## Options

* Migrate closed tickets to the new solution
* Migrate open tickets to the new solution
* create new tickets in the new system, tickets created in the old solution should be left in the current solution

# Decision

Migration of closed tickets is not advisable:

The closed tickets are mostly accessed in reference to the knowledge base
Information on tickets can be obtained in the old systems by administrators

In the first stages, it is planned to start new tickets in the new system, and to work with the old ones in the current implementation. Reasons for the decision:

It is supposed that the lifetime of open tickets is not long.
The main problems to be solved are related to open tickets
Avoiding migration of tickets from the old system will reduce time and avoid problems with duplicate information
If necessary, some of the old tickets can be recreated in the new components in manual mode

# Consequences

In the first stages, 2 versions of the ticketing interface should be available to operators

When designing the new knowledge base architecture, it is necessary to provide a loosely coupled knowledge base system and ticket management components. The new knowledge base component should contain information from tickets for decision making and not require the old components to work