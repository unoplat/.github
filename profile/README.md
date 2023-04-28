![unoplat-logo](https://user-images.githubusercontent.com/17126168/233903694-4dd29b28-ad00-4169-8e78-9a404defe397.PNG)




# Table of Contents

1. [What is UnoPlat](#what-is-unoplat)
2. [Current state of Data Platforms](#current-state-of-data-platforms)
3. [Why UnoPlat](#why-unoplat)
4. [UnoPlat Composition](#unoplat-composition)
5. [UnoPlat Workflow](#unoplat-workflow)
6. [UnoPlat - Sample Implementation: DataPlatform - Ride Hailing Apps](#unoplat-sample-implementation)
7. [About Us](#about-us)

## What is UnoPlat

UnoPlat, a cutting-edge datamesh inspired data platform designed to revolutionize the way businesses access, manage, and derive value from their data. As a comprehensive and innovative solution, UnoPlat is perfectly positioned to become a key platform, helping you enhance your data-driven offerings and services.

At a high level, UnoPlat is a data platform that offers:

- Domain-oriented architecture: UnoPlat enables decentralized data ownership, allowing businesses to scale out their data ecosystem while maintaining autonomy and control over their domain-specific data.
- Data as a product: Our platform emphasizes treating data as a valuable product, ensuring easy discoverability, secure access, and high-quality data that can be consumed and utilized seamlessly across the organization.
- Self-serve infrastructure: UnoPlat empowers domain teams to create and consume data products autonomously through a user-friendly, self-serve data infrastructure. This dramatically reduces the complexity associated with building, executing, and maintaining data products.
- Federated computational governance: Our platform facilitates interoperability between independent data products while respecting domain autonomy. UnoPlat's governance model supports adherence to global standards and ensures a healthy, interconnected data ecosystem.

## Current state of Data Platforms

Current data platforms face several challenges that limit their effectiveness in meeting the demands of today's data-driven organizations. Key pain points include:

- Engineering: Traditional platforms often rely on closed looped architectures, making them difficult to scale and adapt to new data sources or use cases. This leads to increased complexity, technical debt, and cost. As none of these platforms are open source, vendor lock-in and maintenance nightmares often cripple the project.
- Management: Centralized data management based on data warehouse and lakes approaches result in bottlenecks, slowing down decision-making and hindering cross-domain collaboration. This stifles innovation and limits the potential for data-driven insights.
- Cost of Production, Creation, and Maintenance: Legacy data platforms require significant upfront investment and ongoing maintenance costs. These platforms can be resource-intensive and difficult to maintain, driving up overall costs.
- Time to Value: The rigid nature of traditional platforms can delay the time it takes to derive value from data. This impacts an organization's ability to make timely, informed decisions and capitalize on opportunities.
- Data Freshness and Collaboration: Conventional data platforms struggle to accommodate the demand for real-time data and seamless data sharing. This hampers organizations from leveraging the full potential of their data assets for better decision-making.
- Data Democracy: Traditional data platforms can hinder data access and democratization, restricting the ability of employees at all levels to make data-driven decisions. Often, collaboration is done on data through a separate tool compared to the one where the data is available, which makes the discussion disconnected and auto-discovery of data difficult.

The shortcomings of existing data platforms make them ill-suited for modern data-driven organizations that require agility, scalability, and collaboration. UnoPlat addresses these challenges, offering a more efficient and adaptable solution for today's data-intensive businesses.


## Why UnoPlat

Moving to UnoPlat offers several advantages to data-driven organizations, providing a more efficient and flexible solution than conventional data platforms. Key benefits include:

- **Architecture**: UnoPlat embraces a modern, domain-oriented decentralized architecture, allowing for better scalability and adaptability to changing business requirements. This ensures that organizations can easily grow and evolve without being held back by rigid data platform limitations.
- **Ease of Adoption**: UnoPlat is designed with a self-serve data infrastructure in mind, enabling teams to quickly onboard and start using the platform. This reduces friction and accelerates time-to-value for organizations transitioning to a new data platform.
- **Ease of Data Generation**: With its data-as-a-product approach, UnoPlat simplifies the process of generating high-quality data products. Teams can focus on delivering valuable data assets that are easy to discover, understand, and use securely by others in the organization.
- **Ease of Maintenance**: UnoPlat's emphasis on automation and self-service capabilities reduces the burden of maintaining complex data pipelines and infrastructure. This allows organizations to allocate resources more efficiently and focus on core business objectives.
- **Ease of Collaboration**: UnoPlat's federated computational governance model promotes cross-domain collaboration, enabling teams to work together seamlessly and derive more value from aggregated and correlated data. This fosters a culture of data-driven decision-making and innovation.
- **Developer Joy**: UnoPlat's modern architecture, self-service capabilities, and focus on automation lead to a more enjoyable development experience for engineers. This increases productivity and job satisfaction while attracting and retaining top talent in the organization.
- **Open Source**: Unoplat is based on Apache License 2.0 due to key advantages: community involvement, transparency, lower costs, flexibility and customization, interoperability, vendor independence, rapid innovation, positive network effects, and educational value. These factors contribute to accelerated development, increased trust, cost-effectiveness, customization freedom, seamless integration, reduced reliance on single vendors, faster innovation, continuous growth, and learning opportunities.

Adopting UnoPlat provides data organizations with a more flexible, scalable, and collaborative solution than traditional data platforms. By addressing the pain points of legacy systems, UnoPlat enables organizations to unlock the full potential of their data assets and drive better decision-making and innovation.

## UnoPlat Composition

UnoPlat, with its cloud-native foundation, focuses on extensibility, configurability, and embracing the core principles of Data Mesh. By leveraging a combination of open-source tools and technologies, UnoPlat offers a flexible and customizable data platform solution that aligns with the rapidly changing distributed systems landscape.

At its core, UnoPlat utilizes Kubernetes as the orchestration medium, deploying a fleet of toolkits that enable the creation and management of a Data Mesh. 
UnoPlat is composed of a collection of planes as show in fig:
![unoplat-composition](https://user-images.githubusercontent.com/17126168/234077800-383349b5-b6e7-4200-9dfe-14d0a5d5c7a2.png)

- **Infrastructure Plane**: Manages the data infrastructure using tools like Kubernetes, IaC, Apache Flink, PostgreSQL, MongoDB, ScyllaDB, Strimzi Kafka Operator, Apache Kafka, and Redpanda.
- **Networking & Policy Plane**: Handles networking, authorization, and data access using Open Policy Agent (OPA), Consul (Service Mesh), and KrakenD (API Gateway).
- **Monitoring Plane**: Facilitates logging, tracing, and monitoring through Signoz, Prometheus Operator, and Grafana Operator.
- **Developer Plane**: Focuses on developer joy, quick feedback, and seamless development using tools like GitHub Actions, FluxCD, Spotify Backstage, k6, Great Expectations, and OpenMetadata.
- **Administration Plane**: Provides a Kubernetes-native architecture for administration, using UnoPlat API Server as a singular API interface to interact with the various planes and their toolchains.
- **Generative Plane**: Offers two interactive modes - UnoPlat CLI for API server capabilities and a natural language-based UnoPlat prompt for easier administration, management, operations, and development.
Together, these planes create a robust, scalable, and developer-friendly data platform that simplifies data management, collaboration, and orchestration.

The backend toolkit of UnoPlat is highly configurable, allowing organizations to choose from an extensive catalog of options to build their ideal data platform.
A preferred backend catalog configuration for UnoPlat includes:

1. Compute Infrastructure: [CIVO Kubernetes](https://www.civo.com/kubernetes)
2. IaC ToolChain: [Pulumi](https://www.pulumi.com/)
3. Message Broker Infrastructure: [Redpanda](https://vectorized.io/redpanda/), [Apache Kafka - Strimzi Operator](https://strimzi.io/)
4. Microservice Framework: [Quarkus JVM/Native](https://quarkus.io/)
5. Serverless Framework: [Knative](https://knative.dev/)
6. BPMN Frameworks: [Netflix Conductor](https://netflix.github.io/conductor/), [Nussknacker](https://nussknacker.io/)
7. Streaming & Batch Infrastructure: [Apache Flink](https://flink.apache.org/)
8. NoSQL Storage Infrastructure: [MongoDB](https://www.mongodb.com/), [Cassandra](https://cassandra.apache.org/), [Scylla](https://www.scylladb.com/)
9. SQL Storage Infrastructure: [PostgreSQL](https://www.postgresql.org/), [CockroachDB](https://www.cockroachlabs.com/)
10. Observability: [Prometheus Operator/Grafana](https://github.com/prometheus-operator/prometheus-operator), [Signoz](https://signoz.io/) ([OpenTelemetry](https://opentelemetry.io/))
11. Feature Engineering Infra: [Feast](https://feast.dev/)
12. GitOps Infra: [GitHub Actions](https://github.com/features/actions)
13. Deployment & Reconciler Infra: [FluxCD](https://fluxcd.io/)
14. Developer Experience ToolChain: [VSCode](https://code.visualstudio.com/), [Tilt(Precommit CI/CD)](https://tilt.dev/), [MkDocs](https://www.mkdocs.org/), [Mermaid](https://mermaid-js.github.io/mermaid/)
15. Developer Portal Infrastructure: [Spotify Backstage](https://backstage.io/)
16. Data Discovery Infrastructure: [OpenMetadata](https://www.openmetadata.org/)
17. Data Quality Check Infrastructure: [Great Expectations](https://greatexpectations.io/)
18. Compliance Infrastructure: Policies as Code - [OPA](https://www.openpolicyagent.org/)
19. Software Supply Chain Compliance: [SLSA](https://slsa.dev/)
20. Performance Engineering: [k6](https://k6.io/)
21. Chaos Engineering: Future (Yet to be decided)
22. Service Mesh Infrastructure: [Istio](https://istio.io/), [Consul](https://www.consul.io/)
23. User Facing Analytics - [Apache pinot](https://pinot.apache.org/)

*Note: The above set of open source tools/frameworks is subjected to change based on market demand and community feedback.*

By composing this optimal set of open-source tools and technologies, UnoPlat empowers organisations to  build and maintain a modern, scalable, and highly configurable Data Mesh. This flexibility ensures that UnoPlat remains relevant and adaptable to the ever-evolving demands of data-driven organizations.

## UnoPlat Workflow

UnoPlat's objective is to optimize the data engineering workflow from the initial data demand request to its fulfillment. By leveraging the various toolkits in the backend catalog, UnoPlat simplifies each stage of the workflow. Here's a brief overview of how UnoPlat streamlines the data engineering workflow:

### Data Consumption
For stateful workflows using streaming and batch processing tools like Apache Flink and Apache Kafka/Redpanda, UnoPlat enables seamless data consumption from various data sources while ensuring data consistency and fault tolerance. For Stateless workflows, consumers of UnoPlat can also use Knative for serverless and Quarkus for microservice use cases apart from Flink.

### Data Source Identification
UnoPlat uses the metadata cataloging tools like OpenMetadata to manage data sources and their respective schemas. This allows teams to easily discover and identify relevant data sources for their use cases.

### Data Cleansing
UnoPlat leverages data quality tools like Great Expectations (integrated with OpenMetadata) to perform data cleansing tasks, such as data validation, deduplication, and data type conversion, ensuring that the data is accurate, consistent, and reliable.

### Metadata Cataloging
UnoPlat utilizes OpenMetadata for metadata cataloging, enabling teams to discover, understand, and collaborate on data assets. This ensures that data remains up-to-date, well-documented, and easily accessible.

### Data Query
Parallel Data Query Python SDKs would be developed based on storage mechanism. This is to ease doing rapid PoCs/MLOps around datasets of choice selected through OpenMetadata.

### Data Versioning, Lineage, and Cataloging
UnoPlat utilizes OpenMetadata for metadata cataloging, data versioning, data lineage, and data discovery. This enables teams to discover, understand, and collaborate on data assets while managing changes to data over time. With OpenMetadata, data remains up-to-date, well-documented, and easily accessible, and it allows for efficient data rollback, historical data analysis, and data lineage tracking.

### Data Products Publishing
By leveraging the self-serve data infrastructure and the platform's built-in observability, UnoPlat ensures that published data products are secure, reliable, and scalable. Data products can be accessed and consumed by various teams across the organization, promoting data democratization and collaboration.

UnoPlat optimizes the data engineering workflow by simplifying each stage and enabling seamless collaboration, leading to faster time-to-value and more effective data-driven decision-making.

## Reference Implementation - UnoPlat for Ride-Hailing Apps

To create a domain-driven data platform for a fictional ride-hailing company using UnoPlat, we will first identify the key domains and then design data products to support those domains. Here's a high-level overview of the data platform architecture for this company on UnoPlat.

### Key Domains:
1. **Customer Domain**: Manages customer profiles, preferences, and ride history.
2. **Driver Domain**: Manages driver profiles, vehicle details, and driver availability.
3. **Ride Domain**: Manages ride requests, matching, ride status, and payments.
4. **Pricing Domain**: Manages dynamic pricing, promotions, and discounts.
5. **Location Domain**: Manages location tracking and geolocation data for drivers and customers.

### Data Products:
1. **Customer Data Product**: Contains customer-related data such as demographics, preferences, and ride history. This data product can be used for personalized marketing, customer segmentation, and churn prediction.
2. **Driver Data Product**: Contains driver-related data such as driver profile, vehicle details, ratings, and availability. This data product can be used for driver recruitment, retention strategies, and driver performance analysis.
3. **Ride Data Product**: Contains ride-related data such as ride requests, ride status, ride duration, distance, and payments. This data product can be used for ride pattern analysis, demand forecasting, and revenue optimization.
4. **Pricing Data Product**: Contains pricing-related data such as dynamic pricing, promotions, and discounts. This data product can be used for pricing strategy, revenue management, and promotional analysis.
5. **Location Data Product**: Contains location-related data such as driver and customer geolocation, route optimization, and traffic data. This data product can be used for route optimization, location-based marketing, and traffic pattern analysis.
