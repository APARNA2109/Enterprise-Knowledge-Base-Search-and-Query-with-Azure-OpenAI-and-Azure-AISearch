# Exercise 2: Query and retrieval 

## Task 1: Create and deploy a web app from a Docker image 


1. Click on the **+ Create a resource** button on the top left corner of the Azure Portal.

    ![](./media/24-07-2024(41).png)

1. In the search box, type **Web App (1)**, select **Web App (2)** from the list of results and click on **Create (3)**.

    ![](./media/24-07-2024(42).png)

1. On the **Basics** tab of **Create Web App** resource page, enter the following settings and click on **Next : Database > (7)** button.
   
    - **Subscription (1)**: Default - Pre-assigned subscription.
    
    - **Resource group (2)**: Select Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Name (3)**: Webapp-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Publish (4)**: Choose **Container**
   
    - **Operating System (5)**: Choose **Linux**
   
    - **Region (6)**: Select **<inject key="Region" enableCopy="false" />**

      ![](./media/24-07-2024(43).png)

    - **Linux Plan (6)**: Select existing plan i.e. **hostingplan-<inject key="Deployment ID" enableCopy="false"></inject> (B3)**

      ![](./media/24-07-2024(44).png)

1. On the **Database** tab, leave the value as default and click on **Next : Container >** button.

1. On the **Container** tab, enter the following settings and click on **Next : Review + create > (4)** button.

   - **Image Source (1)**: Select Docker Hub or other registries

   - **Access Type (2)**: Select Public

   - **Image and tag (3)**: Enter fruocco/oai-batch:latest

     ![](./media/24-07-2024(45).png)

1. On the **Review + submit** tab, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(46).png)

1. Once the deployment is complete, click on the **Go to resource** button.
   
    ![](./media/24-07-2024(47).png)

1. 