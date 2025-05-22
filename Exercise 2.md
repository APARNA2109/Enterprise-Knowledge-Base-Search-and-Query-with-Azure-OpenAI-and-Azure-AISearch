# Exercise 2: Query and retrieval

### Estimated Duration: 120 minutes

In this exercise, you will create and deploy a web application from a Docker image in Azure, configure environment variables, and test the deployment.

## Lab objectives

In this exercise, you will complete the following tasks:

- Task 1: Create and deploy a web app from a Docker image
- Task 2: Add environment Variables and check the Docker deployment
- Task 3: Test the web app

## Task 1: Create and deploy a web app from a Docker image

In this task, you will create a new Azure Web App resource. The web app will be set up to use a Docker container from a specified image. You will configure the app with settings for subscription, resource group, and Linux plan, and then deploy the Docker image **fruocco/oai-embeddings:latest** to the web app.

1. Click on the **+ Create a resource** button in the top left corner of the Azure Portal.

    ![](./media/24-07-2024(41).png)

1. In the search box, type **Web app (1)**, select **Web App (2)** from the list of results and click on **Create (3)**.

    ![](./media/24-07-2024(42).png)

1. On the **Basics** tab of **Create Web App** resource page, enter the following details and click on **Next : Database > (9)** button.
   
    - Subscription: **Default - Pre-assigned subscription (1)**
    
    - Resource group: Select **Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject> (2)**
    
    - Name: **Webapp-<inject key="Deployment ID" enableCopy="false"></inject> (3)**

    - Secure a unique default hostname: **Turn off (4)**
    
    - Publish: Choose **Container (5)**
   
    - Operating System: Choose **Linux (6)**
   
    - Region: Select **<inject key="Region" enableCopy="false" /> (7)**

    - Linux Plan: Select an existing plan i.e. **hostingplan-<inject key="Deployment ID" enableCopy="false"></inject> (B3)**  **(8)**

      ![](./media/webapp1.png)

1. On the **Database** tab click on **Next : Container >**

1. On the **Container** tab, enter the following details and click on **Review + create (4)** button.

   - Image Source: Select **Other container registries (1)**

   - Access Type: Select **Public (2)**

   - Image and tag: Enter **fruocco/oai-embeddings:latest (3)**

     ![](./media/webapp2.png)

1. On the **Review + create** tab, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(46).png)

1. Once the deployment is complete, click on the **Go to resource** button.
   
    ![](./media/24-07-2024(47).png)

## Task 2: Add environment Variables and check the Docker deployment

In this task, you will configure the necessary environment variables. This involves accessing the environment variables section in the web app settings, editing the values to match those provided in the previous exercise, and saving the changes.

1. In the left-hand menu, select **Environment variables (1)** under **Settings section** and click on **Advanced edit (2)** at the top of the page to view or modify the environment variables.

    ![](./media/lab-04.png)

1. In the advanced editor, delete the current values and paste the new values you copied from the Function App in the previous exercise. Then, click **OK**.

    ![](./media/24-07-2024(50).png)

1. Click on **Apply** and then select **Confirm** to save the changes.

    ![](./media/18.png)

    ![](./media/19.png)

### Task 3: Test the web app

In this task, you will test the functionality of the deployed web app by browsing it through the Azure Portal.

1. Now, go to the **Overview** of the Azure Web App, and click on **Browse (2)** to open the web app.

    ![](./media/24-07-2024(51).png)

    > **Note**: If you encounter any errors while opening the web app, restart the web app, wait for 2-3 minutes, and then try again.

1. After the cold-start delay while your app's Docker image loads and starts, you'll see a page like the following image:

    ![](./media/24-07-2024(52).png)

1. In the left-hand menu, select **Add Document (1)** and then click on **Browse files (2)**.

    ![](./media/24-07-2024(53).png)

1. Navigate to `C:\LabFiles` **(1)**, select **sample-layout (2)** file and click **Open (3)**.

    ![](./media/20.png)

1. Once the file is uploaded, you'll see a page like the following image:

    ![](./media/24-07-2024(54).png)

1. To confirm, in the Azure Portal, type **Storage accounts (1)** in the search box and select **Storage accounts (2)** from the results.

    ![](./media/21.png)

1. On the Storage accounts page, select **storage<inject key="Deployment ID" enableCopy="false"></inject>**.

    ![](./media/22.png)

1. In the left-hand menu, select **Containers (1)** under **Data storage** section and open the **documents (2)** container.

    ![](./media/23.png)

1. Verify that the **sample-layout** file has been added to this container. You should also see a folder named **converted**, which contains the text version of the file processed by the Azure Functions.

    ![](./media/24.png)

    ![](./media/25.png)

1. Return to the web app page, click on **Chat** and ask a question related to the **sample-layout** file. Below are the questions you can ask:

    ```
    Give me an overview about sample layout
    ```

    ![](./media/37.png)

1. You can click on **Sources** to obtain the converted file in text format.

    ![](./media/38.png)

    ![](./media/39.png)

1. From the JumpVM, open **File Explorer** by selecting its icon on the Windows Taskbar.

    ![](./media/12.png)

1. Navigate to `C:\LabFiles` **(1)** and double-click on the `Emil und die Detektive book` **(2)** file to open it.

    ![](./media/28.png)

1. Once the file is opened, verify that it is in the **German language**. We will then use the web app to translate the file into English and obtain the results using OpenAI Chat.

1. Return to the web app page, in the left-hand menu, select **Add Document (1)**, check the box for **Translate document to English (2)** and then click on **Browse files (3)**.

    ![](./media/29.png)
    
1. Navigate to `C:\LabFiles` **(1)**, select **Emil und die Detektive book (2)** file and click **Open (3)**.

    ![](./media/31.png)

1. Once the file is uploaded, you'll see a page like the following image:

    ![](./media/32.png)

1. To confirm, return to the **storage<inject key="Deployment ID" enableCopy="false"></inject>** and open the **documents** container. Verify that the **Emil und die Detektive book** file has been added to this container. You should also see a folder named **converted**, which contains the text version of the file processed by the Azure Functions.

    ![](./media/33.png)

    ![](./media/34.png)

1. Return to the web app page, click on **Chat** and ask a question related to the **Emil und die Detektive book** file. Below are the questions you can ask:

    ```
    Give me an overview about this book
    ```

    ![](./media/36.png)

    ```
    What is the name of the main character in the book?
    ```

    ![](./media/35.png)

    ### How the File Translation is Managed?

    - The end-to-end process of managing and querying a knowledge base using Azure services. The workflow includes the following key steps:

        - **Knowledge Base Storage**:
            - **Azure Storage**: Stores unstructured documents such as PDFs, DOCX, and TXT files, providing a scalable and secure repository.

        - **Data Extraction**:
            - **Azure Document Intelligence**: Automatically extracts paragraphs and dialogues from the raw documents, converting unstructured data into structured formats for further processing.
            
            - **Azure Translator**: Translates extracted text into the desired language, ensuring the system can handle multilingual queries and documents.

        - **Text Embedding and Indexing**:
            - **Azure OpenAI Service Embeddings**: Converts the extracted text into high-dimensional vectors, encapsulating semantic meaning and context.
            
            - **Azure AI Search**: Indexes these embeddings, enabling fast and efficient vector-based searches across the knowledge base.

        - **Search and Answering**:
            - **Vector Search**: Uses Azure OpenAI Embeddings to perform a semantic search, matching user queries to the most relevant documents based on vector similarity.
            
            - **Azure AI Search**: Retrieves the top k relevant paragraphs from the indexed documents.

            - **Azure OpenAI Answering Prompt**: Constructs a concise and contextually accurate response from the retrieved paragraphs. If required, answers can be translated back to the user's preferred language.

1. You can click on **Sources** to obtain the converted file in text format.

    ![](./media/40.png)

    ![](./media/41.png)

## Summary

In this exercise, you have accomplished the following:

- Created and deployed a web app from a Docker image
- Added environment variables and checked the Docker deployment
- Tested the web app

### You have successfully completed the lab.
