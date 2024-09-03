# domains

domains are the area of application your application works within.

## models
* interpretation of the domain
* models are always wrong
* but some are useful
* we don't model reality, we model useful abstractions

## ubiquitous language
* a language structured around the domain model
* used by the team members and throughout the code

## bounded context
* an explicit boundary within which a domain model exists
* inside all terms have a specific meaning
* they are part of ubiquitous language
* high cohesion (things that work together stick together)
* loose coupling (things rely as little as possible on each other)
* represents business capability
* context-specific model

> we don't want to build a model that works for everyone

> we don't design a one-size-fits-all architecture, because it doesn't fix
> anything well.

## microservices
* invidividual persistance
* individual tech stacks
* individual deplyability
* individual replacability
* individual scalability
* can fail individually

## what are microservices about?
* free choice of architecture
* free choice of persistance
* free choice of language

