202204250832
Status: #idea
Tags: [[Data Activation]], [[Reverse ETL]], [[Operational Analytics]]
Links:
## Topic
>Eventually, we built the six frameworks that became Data Activation:
>

**Objects**:
    -   Description: syncing data from one table to another table, and mapping columns from the source model to the destination
    -   Common destinations: Sales CRMs (Salesforce, Hubspot), Marketing CRMs (Braze, Iterable), Intercom, ERPs & finance tools (Netsuite and Anaplan), and 70+ more. This also includes database destinations like Postgres and --- MongoDB (for in-app personalization).
    -   Example Use Case: Sync product engagement data from the warehouse into Salesforce. Sales needs to see how much a customer has consumed and which features they’ve interacted with so that they can sell the right features and limits.

**Event syncing**:
    -   Description: syncing event data into destinations that allow analysis or action on events. The user selects the object on which the events are performed. Hightouch will store the timestamp of the latest event during each sync so that only newer data is pulled from the database, which speeds these syncs up considerably.
    -   Common destinations: Amplitude, Mixpanel, Braze events, and Iterable events
    -   Example Use Case: Sync purchase event data to Braze so that marketers can automatically enroll buyers of specific products in relevant email campaigns, based on the color and category of the purchased product.

 **[Hightouch Notify](https://hightouch.io/notify/)**:
    -   Definition: send messages to internal team members or to customers directly, triggered by data in the warehouse
    -   Common destinations: Slack, Mattermost, and Microsoft Teams
    -   Example Use Case: Any time a customer workspace surpasses the limit of the free tier, send a message in Slack tagging the relevant salesperson and notifying them that they should reach out and ask the workspace to pay (PQLs).

![image6.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/image6_05fc16bb1e.png)

 **[Hightouch Audiences](https://hightouch.io/audiences/)**:
    -   Definition: Maintain a list of users in destinations that have audience lists. Both create users as they enter the audience, and delete users as they leave the audience.
    -   Common destinations: Facebook Audiences, Google Ads, Bing, Tik Tok, Snapchat, Mailchimp, Sendgrid, SFMC
    -   Example Use Case: When someone fills out a coupon form and enters their email address, upload their email to a Facebook, Google, and Tik Tok audience so that they receive ads about products they’re interested in. When they purchase a product, remove them from all three audiences.

![image1.png](https://www.master-7rqtwti-od3d6y3dmsppq.us-4.platformsh.site/uploads/image1_4f2e1c393f.png)

**File Uploads**:
    -   Definition: Download the results of a query as a file, and upload the file to an external storage bucket. That storage bucket could be internal-facing or client-facing.
    -   Common Destinations: SFTP, S3
    -   Example: Clients run ads on an advertising platform. The identities of clicking users are stored in the advertising platform’s data warehouse and shared with the clients via SFTP.

**Tasks**:
    -   Definition: Automatically create tickets or tasks based on rules defined by a SQL query or model. Only create that ticket or task once for each user, even if the action is performed twice. Currently, this framework fits under ORM, but it may be split out.
    -   Common Destinations: Asana, Jira, Zendesk, Salesforce
    -   Example Use Case: Query workspaces that just graduated from 4 users to 5 users (PQL). Automatically create a task in the helpdesk tool (Jira or Zendesk) so that a support rep can reach out to the workspace and ask if they need help setting up any premium features.

>Each customer of Hightouch uses the product in a different way, and the majority eventually graduate to doing more than Reverse ETL:
>-   [Vendr](https://hightouch.io/customers/vendr) automates customer touchpoints
>-   [Compare Club](https://hightouch.io/customers/compare-club) reduced cost per lead by 10%
>-   [Retool](https://hightouch.io/customers/retool) increased email response rates by 32%.
>-   [Circle CI](https://hightouch.io/customers/circleci) activates dbt models to measure ROI
>-   [Blend](https://hightouch.io/customers/blend) reduced reporting time by 50%
>-   [Nando’s](https://hightouch.io/customers/nandos) improves customer loyalty & reduces data integration time by 75%


___
#References
https://hightouch.io/blog/the-data-activation-company/
