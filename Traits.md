
## isolated
## scalable
## resilient
>   the ability to heal from failure

## cohesive

## Bulkheading
>   create watertight compartments that can contain water in the case of a hull breach or other leak.

### Failure isolation
>   to contain and manage failure without having it cascade throughout the services participating in the workflow—is a pattern sometimes referred to as Bulkheading

## Act Autonomously 
>   Isolation is a prerequisite for autonomy. An autonomous service can only promise6 its own behaviour by pub‐ lishing its protocol/API. Another aspect of autonomy is that if a service only can make prom‐ ises about its own behavior, then all information needed to resolve a conflict or to repair under failure scenarios are available within the service itself, removing the need for communication and coordina‐ tion.


## Event Log

>   An Event Log is a durable storage for the messages. We can either choose to store the messages as they enter the service from the out‐ side, the Commands to the service, in what is commonly called called Command Sourcing. We can also choose to ignore the Com‐ mand, let it perform its side-effect to the service, and if the side effect triggers a state change in the service then we can capture the state change as a new fact in an Event to be stored in the Event Log using Event Sourcing.

>   Transaction logs record all the changes made to the database. High-speed appends are the only way to change the log. From this perspective, the contents of the database hold a caching of the latest record values in the logs. The truth is the log. The database is a cache of a subset of the log. That cached subset happens to be the latest value of each record and index value from the log.

## Event Sourcing

## CQRS - Command Query Responsibility Segregation


### Polyglot Persistence
