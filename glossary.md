## isolated
## scalable
## resilient
>   the ability to heal from failure
## cohesive
## reactive? [Reactive Manifesto](http://www.reactivemanifesto.org/)
### share-nothing architecture
### allow concurrency
### allow distribution & mobility
### 
## Bulkheading
>   create watertight compartments that can contain water in the case of a hull breach or other leak.
### Failure isolation
>   to contain and manage failure without having it cascade throughout the services participating in the workflow—is a pattern sometimes referred to as Bulkheading
## Act Autonomously 
>   Isolation is a prerequisite for autonomy. An autonomous service can only promise6 its own behaviour by pub‐ lishing its protocol/API. Another aspect of autonomy is that if a service only can make prom‐ ises about its own behavior, then all information needed to resolve a conflict or to repair under failure scenarios are available within the service itself, removing the need for communication and coordina‐ tion.
## SRP - Single Responsibil‐ ity Principle
>   Unix Philosophy - Do One Thing, and Do It Well
## Bounded Context - DDD Principle

>   When communicating with another Microservice, across Bounded Contexts, you can only ask politely for its state—you can’t force it to reveal it. Each service responds to a request at its own will, with immutable data (facts) derived from its current state, and never exposes its mutable state directly.
>   This gives each service the freedom to represent its state in any way it wants, and store it in the format and medium that is most suitable. Some services might choose a traditional Relational Database Man‐ agement System (RDBMS) (examples include Oracle, MySQL and Postgres), some a NoSQL database (for example Cassandra and Riak), some a Time-Series database (for example InfluxDB and OpenTSDB) and some to use an Event Log11 (good backends include Kafka, Amazon Kinesis and Cassandra) through techniques such as Event Sourcing12 and Command Query Responsibility Segregation (CQRS).

Conway's Law in 1967:
>   Any organization that designs a system (defined broadly) will pro‐ duce a design whose structure is a copy of the organization’s com‐ munication structure.

