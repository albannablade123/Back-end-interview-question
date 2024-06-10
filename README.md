# Back-end-interview-question



### Questions about Service Oriented Architecture and Microservices:

1. What is a Microservice?
* A microservice is a small, independent component of a more extensive application. Each microservice has its own functionality and can be deployed independently.

* Microservices often build into large, complex applications that are easy to maintain and scale. One of the benefits of using microservices is that they can be written in different programming languages and deployed on different servers.Microservices often build into large, complex applications that are easy to maintain and scale. One of the benefits of using microservices is that they can be written in different programming languages and deployed on different servers.

* Common examples of microservices include user authentication, payment processing, and image manipulation.


2. Explain the concept of microservices architecture and its benefits in cloud development.
* Microservices architecture is an architectural style where an application is composed of loosely coupled, independently deployable services.
Benefits of microservices architecture in cloud development include:
    * Agility: Microservices enable faster development cycles and rapid iteration, as teams can independently develop and deploy services without being slowed down by dependencies on other teams or components.
    * Scalability: Cloud platforms provide built-in scalability features that align well with microservices architecture, allowing services to scale up or down dynamically in response to changing workloads.
    * Fault Isolation: Isolating services reduces the blast radius of failures, making it easier to identify and address issues without affecting the entire system.
    * Technology Diversity: Teams can choose the most appropriate technologies for each service, leading to greater innovation and efficiency.

3. What is the ACID principle in database transactions, and why is it important?
* 	Acid Principle is a set of properties that ensure the reliability and consistency of database transaction
    * Atomicity - Guarantees that transaction is a single unit, meaning that either all of its operations are successfully completed or none of them are, so there can be no transaction that have some of the transaction completed while the others have not
    * Consistency - Ensure that transaction modify DB from one valid state to another valid state, the DB remains in a consistent state before and after, adhering to define constraints, rules and relationship
    * Isolation - ensure that the execution of multiple transactions concurrently does not interfere with each other, prevents dirty reads, non-repeatable reads and phantom reads
    * Durability - Ensure that once transaction has been committed, it is permanently stored in the DB and is not lost due to hardware failures, power outages etc.
