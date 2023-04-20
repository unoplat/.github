# Hello World!

We formed the team in late 2018. The objective was to platformize components across multiple product lines.

## Vision

The goal is to take all of the learnings we have had and bootstrap Cloud native Data platform. We call this platform UNOPLAT.AI .

## Metrics of Success

* Time to Value for any feature/product
* To enable data driven use cases by at least an order of magnitude faster through uno data mesh.
* Reduce Operating Cost by at least an order of magnitude.
* Developer Experience

## Approach

Based on the metrics of success, we had to build the foundation for any cloud-native product in any domain. We call this foundation Unoplat.ai.
After multiple case studies and developing backend infra/services for various engineering leaders, we arrived at these cross-cutting concerns:

1. Uno Developer Joy
2. Uno App and Infra Fabric
3. Uno Data Mesh
4. Uno MLOps

### Uno Developer Joy

#### What is Developer joy?

Developer joy stems from keeping developers happy and productive by shielding them from daily chaos, inspired by Spotify's backstage insights. It addresses pain points like unnecessary cognitive load from interacting with multiple tools and slow feedback loops.

#### Why is it needed?

Developers face many day-to-day operations, such as figuring out best frameworks for the task assigned, version control, devsecops, IAM, monitoring tools, etc. Navigating multiple portals creates cognitive load, hindering productivity and creativity. Feedback loops for commit quality are slow, impacting product timelines.

#### How teams could achieve Developer Joy?

By adopting a Kubernetes-like approach for developers, providing a single interface with reusable code, devsecops, monitoring, alerting, infra, and docs. Implementing precommit CI/CD ensures instant feedback on code quality, security, and tests before committing.

#### How does **UNOPLAT** solve this problem?

UnoPlatform is an opinionated platform in terms of its selection of tools and as of now the platform relies on:
1.  **Spotify Backstage.** - Single pane of glass for devs.
2.  **tilt** - Precommit CI/CD
3. **Unoplat Cli**  - To Interact with Unoplat ecosystem

#### References:
* [Spotify Backstage](https://backstage.io)
* [Shifting from Spreadsheets to Backstage](https://www.youtube.com/watch?v=lCgDiusuixM)
* [Reproducible builds and deployments](https://nixos.org)
* [Precommit CI/CD](https://tilt.dev/)
* [Backstage Documentation](https://backstage.io/docs/overview/what-is-backstage)

## Impact on business/Organisation

* Supercharged Development experience resulting in exponential reduction in time to value for shipping products/features and happy devs.

### Uno App and Infra Fabric

#### What is Uno App and Infra Fabric?

Uno App Fabric aims to create reusable software templates, empowering companies to launch features quickly without worrying about cross-cutting concerns in software development.

#### Why is it needed?

Today's tech landscape offers countless software frameworks, message brokers, databases, and monitoring tools. Choosing and managing these components can be overwhelming and requires specialized skills.

Cross-cutting concerns in software development include:

1. High Availability - Ensuring continuous system uptime and minimizing service disruptions.
2. Observability - Metrics, Logging, Alerting, Tracing, and Visualization
3. Scalability - Adapting system capacity to handle increasing workloads efficiently.
4. Fault tolerance - Resilient to failures, Exactly-once semantics wherever applicable.
5. DevSecOps: Integrates development, security, and operations practices to close feeback loop as early as possible.

#### How do organizations approach App and Infra Software Template process?

Before arriving at the solution, it is essential to understand the different categories of software for developing any backend cloud-native feature:

* **Stateful Applications** - Applications that require state to maintain (e.g., Message Brokers, Databases, Stateful Streaming/Batch Apache Flink).
* **Stateless Application** -  Services that don't require state to maintain. For Example - Spring boot/Quarkus based microservices.
* **Operators** - Simplify administration of stateful applications.
* **BPMN-based Applications** - Require state maintenance after every step of a process (e.g., Camunda, Nuss Knacker, Netflix Conductor).

Two examples illustrate the concept of software templates:

1. In a library management system, let us have a look at inventory feature. A microservice template with an HTTP POST endpoint as the source and a SQL DB as the sink, along with pluggable business logic, can be used for inserting book data.

2. For calculating the average pollution in a city over 24 hours, sensors provide data through a message broker. A streaming tumbling stateful service template with a message broker topic as both the source and sink, along with pluggable stateful business logic, can be used to compute the average.

To address cross-cutting concerns of any application, the template should include default features such as:

* MDC-based Logging
* Observability
* Reactive Scaling
* High Availability
* DevSecOps
* Operator-driven 3p components
* Service Mesh
* Unit Tests
* BDD Tests

Software development can be templatized using Directed Acyclic Graphs (DAG) with single/multiple sources and sinks, and stateful/stateless pluggable business logic data processor nodes. By applying the DAG-based approach, developers can create reusable software templates that address a wide range of use cases, streamline development, and improve efficiency.

