202204250957
Status: #idea #case-study 
Tags: [[automation]], [[Reverse ETL]], [[Data Activation]], [[Operational Analytics]]
Links:
## Topic
## Results
>-   With Snowflake, Vendr can support unlimited concurrent users and leverage solutions like Hightouch and dbt to power an assortment of use cases to automate vital touchpoints between Vendr and their customers.
>-   By using Hightouch to send financial data to Google Sheets, Vendr’s Head of Operations now has four extra weeks per year to focus on business outcomes.
>-   Instead of having to manually send individual emails and Slack messages, Vendr automates HubSpot workflows and Slack messages with data from Hightouch to notify buyers and sellers about actions needed to close specific deals.
>-   With Hightouch’s native dbt Cloud integration, every Hightouch Sync happens automatically once its dbt job is completed and the data is updated in Snowflake.
>-   Using dbt, Snowflake, and Hightouch, Vendr sends surveys out to customer-side stakeholders and supplier-side reps.

# About Vendr
>With hundreds of SaaS products in a given company, it’s getting more and more challenging and time-consuming to manage supplier relationships and negotiate contracts. Vendr has completely transformed this entire process by creating a SaaS buying platform where stakeholders can easily handle the relationships and contracts of their different software suppliers in a centralized platform. Vendr also provides unbiased insights of popular tools and upcoming technologies to help inform new purchases.
>
>With SaaS experts called Executive Buyers and insights from thousands of transactions, Vendr has helped companies save a combined $100M in the last two years. Vendr guarantees to save every customer more money than their annual cost and more importantly, save every customer the time and stress usually wasted on back and forth negotiations during a purchase or renewal. In turn, companies have more time and resources to focus on business outcomes, instead of purchasing new software.

# The Challenge: improving scalability and automating sales/marketing processes

>With the proliferation of SaaS companies increasing rapidly during COVID-19, Vendr experienced rapid growth, increasing from 30 employees to over 180 in less than a year. With this rapid expansion, Vendr knew that its technology stack could not maintain this acceleration. Vendr’s technology stack was relatively nascent, consisting of a makeshift PostgresSQL data warehouse, dbt Core, and a self-hosted Metabase instance for business intelligence. As such, Vendr wanted to future-proof its technology stack with solutions that could easily scale to support its many use cases.
>
To broker deals effectively, Vendr needs to communicate with both the seller and buyer. This requires the Customer Success team to reach out multiple times to ensure that both the buyer and seller are taking the appropriate actions required on their end to close the deal, which is very time-consuming. The company needed a centralized data platform and a way to automate this process to save the Customer Success team time.
>
>"Why reinvent the wheel when something has been done a thousand times? I don’t want anyone on my team doing something that has been done before if that can be avoided. Hightouch, Snowflake, and dbt have made my job so much easier."
Erik Edelmann
Sr. Analytics Engineering Manager

# The Solution: centralizing, transforming, and democratizing data for activation
>With this in mind, Vendr’s data team turned to Snowflake on AWS as its centralized data platform, dbt Cloud for data modeling and transformation, and Hightouch for Reverse ETL.

## Snowflake as Vendr’s data strategy backbone
>Implementing Snowflake was the first step in re-architecting Vendr’s technology stack. Using Snowflake, Vendr can easily scale up or down to meet its business requirements and support its many users.

>Vendr chose Snowflake for many reasons, but one of the most important was concurrency. Snowflake’s multi-cluster architecture enables Vendr to elegantly address its concurrency scenarios in a controlled fashion.

>Snowflake also allows Vendr to work with semi-structured data and easily scale up or down with ease. Ultimately, Snowflake acts as the backbone for Vendr’s entire data organization, empowering all employees within the organization.

>"We knew that we were going to run into concurrency issues, so the auto-scaling within Snowflake is vital in supporting our Looker users. Snowflake empowers everything that we do. With Snowflake I don’t have to think about anything, because it just works. It’s easy to use, and as our use cases and challenges evolve and grow, we can depend on it to meet our needs."
Erik Edelmann
Sr. Analytics Engineering Manager

## Modeling data with dbt Cloud and Snowflake
>Vendr leverages dbt Cloud on top of Snowflake to transform and model all of its data for analytics purposes. Using dbt Cloud in parallel with Snowflake, Vendr is able to associate CRM objects (such as companies) with specific product data objects (such as workspaces). Vendr also uses dbt to build data models on top of Snowflake that show how long specific deals have been stuck in different stages.
>
>Vendr also uses dbt to schedule, manage, and automate processing jobs within Snowflake. With dbt Cloud, Vendr leverages continuous integration production code changes and standardizes various processes.
>
>Incremental dbt models enable Vendr to generate automated and personalized messages based on the deal stage and the actions that the customer needs to take to close the deal.

## Activating dbt models with Hightouch
>Snowflake and dbt immediately addressed all of Vendr’s challenges from an analytics standpoint, but operationalizing the data models and insights gained from Snowflake is where Hightouch steps in.

## Automated lifecycle marketing powered by the data warehouse
>Using Hightouch, Vendr is able to sync dbt models of customized messages directly to HubSpot. As soon as the dbt run is complete, the messages are synced to HubSpot. Then, workflows in HubSpot are activated to trigger specific emails (using the messages in the dbt model) to buyers and sellers notifying them of actions that need to be taken to close a deal or renew a contract. These same emails are also used to prompt customers to fill out customer feedback surveys after a deal has closed.
>
>![hubspot_email.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/hubspot_email_050c298a24.png)![automated_feedback_surveys.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/automated_feedback_surveys_70ae8fdb60.png)
>
>"Hightouch really expands the reach of Snowflake for us. Not everyone is doing their work in a BI tool—some of our employees are doing it in a CRM, and that is why Hightouch is valuable."
 Erik Edelmann
Sr. Analytics Engineering Manager

## Automating Slack messages based on product usage data
>Vendr has Slack channels with each customer, so if emails are ineffective, they can escalate messages and send them directly in Slack. Before Hightouch, two people had to spend an entire day every week ensuring these messages went out.
>![slack_escalation.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/slack_escalation_cb08e7561a.png)
>
On top of this, Vendr also created a “Deal Success Bot” that gives credit to employees who save customers over 25% or $100K in savings. This is a huge morale boost to the entire team (see example below), as everyone is aligned on customer value and a more transparent SaaS buying process.
>![slack_success.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/slack_success_fdb6028871.png)
>
>"Creating syncs in Hightouch can take as little as an hour with testing. Because of this efficiency, we now use Hightouch to power a number of important workflows that are used across the entire business."
 Erik Edelmann
Sr. Analytics Engineering Manager

## Automating financial reports with Snowflake
>Before Hightouch, Vendr’s Head of Operations was forced to spend an entire week every quarter building reports in Google Sheets for various financial statements. With Hightouch, this information is now synced directly from its centralized data platform with Snowflake to a spreadsheet, which is then visualized for analysis and communication to Vendr’s board.
>
Best of all, Vendr leverages version control with Hightouch’s native Git integration to ensure all syncs and models are defined and backed up in code. All of its syncs can be easily updated every time there is a change in data models and data.
>
"Data is core to our business. Taking that data and putting it in the right place at the right time is key and that is exactly where Snowflake, Hightouch, and dbt help"
Erik Edelmann
Sr. Analytics Engineering Manager

# What’s Next
>Vendr has big plans for the future. There are many upcoming “data-as-a-product” initiatives to help customers better understand their current SaaS stacks and SaaS spend. Vendr will be making a concerted push toward building and providing product features to help customers make better choices when it comes to purchasing SaaS tools. The team will enhance efforts toward bridging the process gap between SaaS buyers and SaaS sellers by helping suppliers recognize the value that Vendr creates when SaaS transactions are managed and streamlined.


___
#References
https://hightouch.io/customers/vendr/
