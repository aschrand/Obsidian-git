---
created: 2023-01-20T09:44:28 (UTC +01:00)
tags: [data, EA]
source: https://thenewstack.io/the-unfortunate-reality-about-data-pipelines/
author: Jon Fancey
Type: artikel
---
The Unfortunate Reality about Data Pipelines https://thenewstack.io/the-unfortunate-reality-about-data-pipelines/

## ELT and Reverse-ETL Pipelines Reinforce Old Bad Habits

ELT (extract, load and transform) tools also focus on loading the data in a centralized cloud data warehouse or data lake, but unlike traditional ETL tools, the transformations happen in the target system, resulting in reduced physical infrastructure and intermediate staging layers. This allowed for data to be extracted and directly loaded into the data warehouse, improving load times. The final destination, yet again, being the data warehouse.

However, in a modern environment, data doesn’t have just one destination. Other systems and applications in the organization need access to the data. And that’s given rise to a whole new set of tools that reverse the pattern of data movement. A symptom of the centralizing force, [[Reverse-ETL]].

![](https://cdn.thenewstack.io/media/2022/11/e918c548-image-2-e1667404287370.jpg)

While the combination of ELT and rETL tools surface the need to share data back to the operational systems and SaaS applications to power various use cases, these approaches intensify the data problem. Decodable CEO Eric Sammer wrote an excellent article on [the abuse of the data warehouse](https://www.decodable.co/blog/were-abusing-the-data-warehouse-retl-elt-and-other-weird-stuff) and how “putting high-priced analytical database systems in the hot path introduces pants-on-head anti-patterns to supportability and ops.”

## How to Implement a Product Mindset in Your Data

To put your data to work and make it discoverable, accessible, and usable, you have to stop thinking of the flow of data as a sequence of processing steps, where the next step is triggered after the previous step is completed. Instead, your data needs to be a first-class citizen.

You have to think of data as something that’s continuously flowing, continuously being processed and continuously shared, so your systems and applications can react and respond to the data the moment it’s created and the moment it changes.

This requires a shift in your mindset. This requires treating your data as if it were a high quality, ready-to-use product that’s instantly accessible across the organization. It’s consistent everywhere, which means that everyone is using the same data and taking advantage of the latest and greatest data so your operational systems can serve your customers better, your analytical systems can meet the demands of your stakeholders, and your SaaS applications are always up to date.

It’s governed, which means you can track where the data is coming from, where it’s going and who has access to it. You enable the discoverability of data assets through data contracts, so whoever needs access to the data in whatever format can easily subscribe and use it on demand.

![](https://cdn.thenewstack.io/media/2022/11/1856915d-screen-shot-2022-11-02-at-11.55.04-am-e1667404546763.png)

When you apply this kind of product thinking to your data, you begin to accelerate use-case delivery and innovation.

How do you deliver this vision and put your data to work? In a modern enterprise, where immediate access to data is critical to being a competitive differentiator, you need to think of the data movement and access in a fundamentally different way. Your approach to data pipelines has to incorporate five essential components. They are:

-   **Streaming:** Built for real-time data access instead of processing data in batches, so you can deliver a consistent view of the most recent data anywhere it’s needed, in the right format, the moment it occurs. The only way to do this is to adopt data streaming to maintain real-time, high fidelity, event-level repositories of reusable data within your organization, rather than pushing periodic, low fidelity snapshots of data to external repositories. And schemas act as the data contract between the producers and consumers, ensuring data compatibility.

-   **Decentralized:** Supports domain-oriented, decentralized data ownership and architecture, allowing teams closest to the data to create and publish independent data streams that can be shared and reused. At the same time, your teams are empowered with a self-serve data infrastructure platform that enables data streams to be discovered, consumed and shaped into multiple contexts on the fly, and multiplexed and shared from and to any destination, everywhere.

-   **Governed:** Enables you to maintain the delicate balance between centralized standards for continuous data observability, security, policy management and compliance, while providing visibility, transparency and compatibility of your data with intuitive search, discovery and lineage so developers and engineers can innovate faster.

-   **Declarative:** Separates the data flow logic from the low level operational details of how the data will be processed. So instead of describing the flow of data as a sequence of operational steps, you must be able to simply describe the flow of data — where the data comes from, where it’s going and what it should look like along its journey, while the infrastructure automatically flexes to handle changes in data scale.

-   **Developer oriented:** Brings agile development and engineering practices to your pipelines. This means enabling your teams to build modular, reusable data flows that can be tested and debugged in an iterative, automated and orchestrated fashion and independently of production environments. It also means that integrating with version control and CI/CD systems so pipelines can be versioned, forked and deployed into different environments. And lastly, it should enable people with different skills and needs to collaborate on developing pipeline components using tools that support both visual IDEs (integrated development environments) and code editors.

When you reimagine the flow of data in the context of these five foundational principles, you enable data-as-a-product thinking and maximize the usability of data, making it easy for different teams to produce, share and consume trustworthy data assets. Together, these principles reinforce one another to promote data reusability, engineering agility and greater collaboration and trust within the organization.

## How Do You Get Pipelines Right?

The next time you’re building an application that needs to be informed by data, ask yourself if your data infrastructure can support your data needs for real-time, ubiquitous, self-service and governed access to high quality data streams. Question why you need to default your assumption to the status quo, which is batch-oriented, centralized, ungoverned and inflexible. Identify solutions that will help you not only solve your data needs for today, but will also serve your business needs in the future. Here are a few resources to get you started:

-   Learn how innovative companies are adopting a transformational next-gen approach. [Netflix discusses](https://netflixtechblog.com/data-mesh-a-data-movement-and-processing-platform-netflix-1288bcab2873) how it is building its data mesh with a data-streaming platform. Adidas does the same in [this article](https://medium.com/adidoescode/introduction-to-data-mesh-adoption-in-adidas-85b1db812fa2).
-   This [e-book](https://www.confluent.io/resources/ebook/data-mesh-architectures-with-event-streams/) does a fantastic job of explaining how to implement your data mesh with Apache Kafka.
-   Learn more about how leading data-streaming vendors like Confluent, who pioneered the category and are the original creators of Apache Kafka, deliver a new approach to [streaming data pipelines](https://www.confluent.io/streaming-data-pipelines/).
-   Get your hands on a [demo](https://www.confluent.io/resources/demo/demo-how-to-use-confluent-for-streaming-data-pipelines) that shows how to build streaming pipelines between operational databases such as Oracle and MongoDB.

[[Data driven strategy]]