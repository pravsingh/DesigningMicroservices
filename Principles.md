
## DRY

## SRP - Single Responsibility Principle
>   Unix Philosophy - Do One Thing, and Do It Well

## Conway's Law in 1967:
>   Any organization that designs a system (defined broadly) will pro‐ duce a design whose structure is a copy of the organization’s com‐ munication structure.


## Bounded Context - DDD Principle

>   When communicating with another Microservice, across Bounded Contexts, you can only ask politely for its state—you can’t force it to reveal it. Each service responds to a request at its own will, with immutable data (facts) derived from its current state, and never exposes its mutable state directly.

>   This gives each service the freedom to represent its state in any way it wants, and store it in the format and medium that is most suitable. Some services might choose a traditional Relational Database Man‐ agement System (RDBMS) (examples include Oracle, MySQL and Postgres), some a NoSQL database (for example Cassandra and Riak), some a Time-Series database (for example InfluxDB and OpenTSDB) and some to use an Event Log11 (good backends include Kafka, Amazon Kinesis and Cassandra) through techniques such as Event Sourcing and CQRS.

> There are benefits to reap from decentralized data management and persistence—sometimes called Polyglot Persistence. Conceptually, which storage medium is used does not really matter; what matters is that a service can be treated as a single unit—including its state and behavior—and in order to do that each service needs to own its state, exclusively. This includes not allowing one service to call directly into the persistent storage of another service, but only through its API—something that might be hard to enforce program‐ matically and therefore needs to be done using conventions, policies and code reviews.

