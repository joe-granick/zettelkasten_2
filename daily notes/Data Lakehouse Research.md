### What is a data lakehouse?
>In the 80s data warehouses (DW) built on relational database management systems (RDBMS) became the norm for enterprise level business intelligence (BI). DWs imposed a structure on the data that made it easy to query and perform analytics on.
>As volumes of data grew, and methods for extracting insight through Artificial Intelligence  and Machine Learning, the limitations of the traditional DW became glaring. The strict structural requiremnts imposed on data warehouses meant only tabular data could be used. While adequate for traditional BI and reporting, this prevented the possibiltiy of extracting data from unstructured sources like text and video, from which AI/ML methods could now extract unprecedented insights. [[Inmon, Levin 2021]]
>
>Data lakes were developed in repsonse to this predicament.  Data lakes provided a location where all data could be placed regardless of structure, stored ina low cost format like Parquet and ORC. These formats were directly accessible for analytics and AI/ML. Unfortunately the lack of transactional guarentees, quality enforcemnt and governance typically resulted in the data lakes turning into disorganized messes where it was a challenge to actually get the data needed. [[Inmon, Levin 2021]]
>
>Data lakehouses were developed to overcome the limitations of data lakes and data warehouse by merging their respective strengths. Data combine data lakes and data warehouses by using the flexibility of storage provided by data lakes and adding strcture and data management capabilities similiar to data warehouses.
>-   **Transaction support:**  ACID transactions for consistency in environments with concurrent read and write operations.
>
>-   **Schema enforcement and governance:** Lakehouses support traditional data warehouse schemas.
>
>-   **BI support:** Allows BI tools to use source data directly reducing latency, improving recency, and saving cost as a separate copy of the data is no longer necessary for both a data lake and a data warehouse.
>
>-   **Decoupled storage and compute:** Storag and compute use separte cluster so the system can scale to more user and larger data sets.
>
>-   **Openness standard formats:** Enables a variety of tools across the spectrum of BI and AI/ML to directly access the data efficiently.
>
>-   **Support for many structures of data**: Lakehouses supports many forms of data including text, video, semi-structured, and formally structured.
>
>-   **Support for diverse workloads:** Supports workloads across BI, Analytics, AI/ML allowing tools native to these domains draw from the source.
>
>-   **End-to-end streaming:**  No need for a separate system to suppor streaming data for real time applications and reporting.
>[[Lorica et. al 2020]]

### What are the benefits of a data lakehouse?
>Data lakehouses overcome many of the limitations of data warehouses and data lakes. The lakehouse is uniquely able to to manage all of an enetrprises data no matter the format or source. It serve as a location to combine these disparate source, perform advanced analytics with ML like data lakes as well as the traditional reporting and BI workloads that were previously the domain of the DW. Some of the benefits of using a data lakehouse include:
>- Allows direct access using open file formats
>- Open API allows direct access to the dat without the use of proprietary engines avoiding vendor lock-in
>- Supports commonly used Analytics and AI/ML languages including, but not limited to SQL, Python, and R
>- Supports all types of structured and unstruictured data used in machine learning workflows
>- Supports dataframes natively, which are the primary data abstraction for many ML libraires including Tensorflow and Pytorch
>- Supports data versioning for ML experiments
>- Supports schema governance and enforcement with ACID transaction guarentess for structured data workflows used by traditional BI worflows similair to DW
>- Provides scalable low cost object storage like a Data Lakes.  (S3, Blob etc.)
>- [[Lorica et. al 2020]]


### What are the key vendors involved in this space?
> Major players in the data lakehouse space include:
>- Databrick
>- Apache Hudi
>- AWS
>- Google Cloud
>- Starburst
>- Dremio
>[[Bornsetin, Li, Casado 2022]]

### How do data lakehouses benefit your own data analytics
>Data lakehouses provide a central location for all analytics data. Analysts can access the data in the same way using the same BI tools and SQL queries that they are used to using with DWs. Since all the data can be stored in the lakehouse, analysts can now have access to all the raw data rather than what they would normally be limited to in the rigid DW structure. They can now explore the data and build pipelines themselves if they identify something useful. They can also mroe easily use ML models developed by data science and ML engineering teams on any data available.
>[[Armbrust et. al 2021]]