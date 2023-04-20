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
* [Precommit CI/CD]
* [Backstage Documentation](https://backstage.io/docs/overview/what-is-backstage)

## Impact on business/Organisation

* Supercharged Development experience resulting in exponential reduction in time to value for shipping products/features and happy devs.


* Uno App and Infra Fabric

## What is Uno App Fabric?

Uno App Fabric aims to create reusable software templates, empowering companies to launch features quickly without worrying about cross-cutting concerns in software development.

## Why is it needed?

Today's tech landscape offers countless software frameworks, message brokers, databases, and monitoring tools. Choosing and managing these components can be overwhelming and requires specialized skills.

Cross-cutting concerns in software development include:

1. High Availability - Ensuring continuous system uptime and minimizing service disruptions.
2. Observability - Metrics, Logging, Alerting, Tracing, and Visualization
3. Scalability - Adapting system capacity to handle increasing workloads efficiently.
4. Fault tolerance - Resilient to failures, Exactly-once semantics
5. DevSecOps: Integrates development, security, and operations practices to enhance collaboration, automation, and vulnerability detection, streamlining software development and ensuring rapid, secure, and reliable delivery.
6. Framework selection as per use case
7. Base Project Structure
8. Base Documentation Structure

## How do we solve this through Uno App and Infra Fabric?

Software development can be templatized based on Directed Acyclic Graphs (DAG) with single/multiple sources and single/multiple sinks, along with stateful/stateless pluggable business logic data processor nodes in between.

Uno App and Infra Fabric addresses cross-cutting concerns by providing software templates preloaded with features such as MDC-based logging, observability, reactive scaling, high availability, DevSecOps, operator-driven 3rd-party components, service mesh for East-West traffic, unit test templates, and BDD test templates.

## How does UNOPLAT solve this problem?

UnoPlat app fabric software templates are based on:

* Popular DBs - Scylla (NoSql), MongoDB (NoSql), PostgreSQL (Sql), CockroachDB (Distributed Db)
* Message Brokers - Redpanda (Message Broker)
* Micro-service templates based on Quarkus
* Streaming/Batch Stateful/Stateless templates based on Apache Flink
* Observability framework based on SigNoz
* Reactive Scalable framework based on KEDA
* User-facing analytics based on Apache Pinot
* Pre-commit DevSecOps based on Tilt
* Post-commit DevSecOps based on GitHub Actions
* Service mesh based on Istio

## Examples

### Library Management System

A library management system requires a REST API to insert book data. By using a micro-service template with an HTTP POST endpoint as the source and a SQL database as the sink, the required functionality can be achieved.

### Average Pollution Calculation

For calculating the average pollution in a city over 24 hours, data from sensors is collected and made available through a message broker. A stateful streaming template with a tumbling window is used to consume data, perform calculations, and publish results to an output topic.

## Conclusion

Uno App and Infra Fabric's software templates can address any single/multiple source and sink problems by allowing developers to plug in their business logic and data processing components into a standardized, reusable structure. This approach significantly reduces the time and effort required to develop new features or products, ultimately leading to increased efficiency and productivity.













* Seamless collaboration with multiple devs across multiple product teams.
* Happier Devs resulting in lesser attrition.
* Exponential reduction in operating cost in using multiple tools to keep track of the project.
