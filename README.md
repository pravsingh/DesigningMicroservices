# Designing Microservices



## isolated
## scalable
## resilient
>   the ability to heal from failure

## cohesive

## reactive? [Reactive Manifesto](http://www.reactivemanifesto.org/)
### Responsive
>   The system responds in a timely manner if at all possible. Responsiveness is the cornerstone of usability and utility, but more than that, responsiveness means that problems may be detected quickly and dealt with effectively. Responsive systems focus on providing rapid and consistent response times, establishing reliable upper bounds so they deliver a consistent quality of service. This consistent behaviour in turn simplifies error handling, builds end user confidence, and encourages further interaction.

### Resilient
>   The system stays responsive in the face of failure. This applies not only to highly-available, mission critical systems — any system that is not resilient will be unresponsive after a failure. Resilience is achieved by replication, containment, isolation and delegation. Failures are contained within each component, isolating components from each other and thereby ensuring that parts of the system can fail and recover without compromising the system as a whole. Recovery of each component is delegated to another (external) component and high-availability is ensured by replication where necessary. The client of a component is not burdened with handling its failures.

### Elastic
>   The system stays responsive under varying workload. Reactive Systems can react to changes in the input rate by increasing or decreasing the resources allocated to service these inputs. This implies designs that have no contention points or central bottlenecks, resulting in the ability to shard or replicate components and distribute inputs among them. Reactive Systems support predictive, as well as Reactive, scaling algorithms by providing relevant live performance measures. They achieve elasticity in a cost-effective way on commodity hardware and software platforms.

### Message Driven
>   Reactive Systems rely on asynchronous message-passing to establish a boundary between components that ensures loose coupling, isolation and location transparency. This boundary also provides the means to delegate failures as messages. Employing explicit message-passing enables load management, elasticity, and flow control by shaping and monitoring the message queues in the system and applying back-pressure when necessary. Location transparent messaging as a means of communication makes it possible for the management of failure to work with the same constructs and semantics across a cluster or within a single host. Non-blocking communication allows recipients to only consume resources while active, leading to less system overhead.

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


## Event Log

>   An Event Log is a durable storage for the messages. We can either choose to store the messages as they enter the service from the out‐ side, the Commands to the service, in what is commonly called called Command Sourcing. We can also choose to ignore the Com‐ mand, let it perform its side-effect to the service, and if the side effect triggers a state change in the service then we can capture the state change as a new fact in an Event to be stored in the Event Log using Event Sourcing.

>   Transaction logs record all the changes made to the database. High-speed appends are the only way to change the log. From this perspective, the contents of the database hold a caching of the latest record values in the logs. The truth is the log. The database is a cache of a subset of the log. That cached subset happens to be the latest value of each record and index value from the log.

## Event Sourcing

## CQRS - Command Query Responsibility Segregation


### Polyglot Persistence

