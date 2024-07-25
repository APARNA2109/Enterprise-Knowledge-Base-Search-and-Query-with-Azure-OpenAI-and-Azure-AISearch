# Exercise 1: Embedding Creation

## Task 1: Deploy Azure OpenAI and Models

Azure OpenAI offers a web-based portal called **Azure OpenAI Studio** for deploying, managing, and exploring models. Follow these steps to deploy a model using Azure OpenAI Studio:

#### Deploy Azure OpenAI Resource

1. In the Azure portal, type **Azure OpenAI (1)** in the search box and select **Azure OpenAI (2)** from the results.

    ![](./media/24-07-2024(31).png)

1. On **Azure AI services | Azure OpenAI** blade, click on **+ Create**.

    ![](./media/24-07-2024(1).png)

1. On the **Basics** tab of **Create Azure OpenAI** resource page, enter the following settings and click on **Next (6)** button.
   
    - **Subscription (1)**: Default - Pre-assigned subscription.
    
    - **Resource group (2)**: Select Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region (3)**: Select **<inject key="Region" enableCopy="false" />**
    
    - **Name (4)**: Openai-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier (5)**: Standard S0

      ![](./media/24-07-2024(2).png)

1. On the **Network** page, leave the value as default and click on **Next** button.

    ![](./media/24-07-2024(3).png)

1. On the **Tags** page, leave the value as default and click **Next** button.

    ![](./media/24-07-2024(4).png)
  
1. On the **Review + submit** page, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(5).png)

1. Once the deployment is complete, click on the **Go to resource** button.
   
    ![](./media/24-07-2024(6).png)

#### Deploy Models in Azure OpenAI Studio

1. On the Azure OpenAI overview page, click **Go to Azure OpenAI Studio** to navigate to Azure AI Studio.

    ![](./media/24-07-2024(7).png)

1. On the Welcome to Azure OpenAI service page, click on **Create new deployment**.

    ![](./media/24-07-2024(8).png)

1. On the Deployments page, click on **+ Create new deployment**.

    ![](./media/24-07-2024(9).png)    

1. In the Deploy model pop-up, enter the following details and click on the **Create (4)** button.
    
    - **Deployment name (1)**: text-davinci-003

    - **Select a model (2)**: gpt-35-turbo-instruct
    
    - **Tokens per Minute Rate Limit (thousands) (3)**: 40K

      ![](./media/24-07-2024(10).png)

1. Repeat the process to create another deployment with the following details and click on the **Create (4)** button. 

    - **Deployment name (1)**: text-embedding-ada-002

    - **Select a model (2)**: text-embedding-ada-002
    
    - **Tokens per Minute Rate Limit (thousands) (3)**: 40K

      ![](./media/24-07-2024(11).png)

## Task 2: Create Azure AI Search Resources

#### Create AI Search Service

1. In the Azure portal, type **AI Search (1)** in the search box and select **AI Search (2)** from the results.

    ![](./media/24-07-2024(12).png)

1. On the **Azure AI services | AI Search** blade, click on **+ Create**.

    ![](./media/24-07-2024(13).png)

1. On the **Basics** tab of **Create a search service** resource page, enter the following settings:
   
    - **Subscription (1)**: Default - Pre-assigned subscription
    
    - **Resource Group (2)**: Select Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>

    - **Service name (4)**: aisearch-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Location (3)**: Select <inject key="Region" enableCopy="false" />
    
    - **Pricing tier (5)**: Standard

      ![](./media/24-07-2024(14).png)

1. Click on **Review + create** button, review the configuration, and click on **Create** button.

     ![](./media/24-07-2024(15).png)

1. Once the deployment is complete, click on the **Go to resource** button.

    ![](./media/24-07-2024(16).png)

1. On the overview page of the AI Search Search Service, copy the **URL** and store it in a notepad for future use.

    ![](./media/24-07-2024(17).png)

1. In the AI Search blade, click on **Keys (1)** under Settings, copy the **Primary admin key (2)**, and store it in a notepad for future use.

    ![](./media/24-07-2024(18).png)
    
#### Create Document Intelligence Resource

1. In the Azure portal, type **Document intelligence (1)** in the search box and select **Document intelligences (2)** from the results.

    ![](./media/24-07-2024(19).png)

1. On the **Azure AI services | Document intelligence** blade, click on **+ Create**.

    ![](./media/24-07-2024(20).png)

1. On the **Basics** tab of **Create Document Intelligence** resource page, enter the following settings:
   
    - **Subscription (1)**: Default - Pre-assigned subscription.
    
    - **Resource group (2)**: Select Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region (3)**: Select <inject key="Region" enableCopy="false" />
    
    - **Name (4)**: Document-intelligence-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier (5)**: Standard S0

      ![](./media/24-07-2024(21).png)
        
1. Click on **Review + create** button, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(22).png)

1. Once the deployment is complete, click on the **Go to resource** button.

    ![](./media/24-07-2024(23).png)

1. In the Document intelligence resource, select **Key & Endpoint (1)** from the left menu, click **Show Keys (2)**, copy **KEY 1 (3)** and the **Endpoint (4)**, and store them in a notepad for later use.

    ![](./media/24-07-2024(24).png)

#### Create Translator Resource

1. In the Azure portal, type **Translators (1)** in the search box and select **Translators (2)** from the results.

    ![](./media/24-07-2024(25).png)

1. On the **Azure AI services | Translator** blade, click on **+ Create**.

    ![](./media/24-07-2024(26).png)

1. On the **Basics** tab of **Create Translator** resource page, enter the following settings:
   
    - **Subscription (1)**: Default - Pre-assigned subscription.
    
    - **Resource group (2)**: Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region (3)**: Select <inject key="Region" enableCopy="false" />
    
    - **Name (4)**: Translator-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier (5)**: Standard S1 (Pay as you go)

      ![](./media/24-07-2024(27).png)
    
1. Click on **Review + create** button, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(28).png)

1. Once the deployment is complete, click on the **Go to resource** button.
   
    ![](./media/24-07-2024(29).png)

1. In the Translator resource, select **Key & Endpoint (1)** from the left menu, click **Show Keys (2)**, copy **KEY 1 (3)** and the **Endpoint (4)**, and store them in a notepad for later use.

    ![](./media/24-07-2024(30).png)

## Task 3: Deploy Azure function with embeddings

1. From the JumpVM, open **File Explorer** by selecting its icon on the Windows Taskbar.

1. Navigate to `C:\LabFiles\` and double-click on the `deploy.json` file to open it. Copy the template to deploy.


1. Navigate back to the Azure Portal, type **Deploy from a custom template (1)** in the search box and select **Deploy from a custom template (2)** from the results.

    ![](./media/24-07-2024(32).png)

1. Paste the template you copied in step number 2 and click on **Save** button.

    ![](./media/24-07-2024(33).png)

1. On the **Basics** tab of **Custom deployment** page, enter the required details given below:

    |Variables	|Values|
    |---|---|
    |Subscription | Default - Pre-assigned subscription |
    |Resource group | Openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Region | <inject key="Region" enableCopy="false" /> |
    |Azure Cognitive Search | aisearch-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Azure Cognitive Search Sku | Standard |
    |Hosting Plan Name | hostingplan-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Hosting Plan Sku | B3 |
    |Storage Account Name | storage<inject key="Deployment ID" enableCopy="false"></inject> |
    |Function Name | Functionapp-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Application Insights Name | Application-insights-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Form Recognizer Name |Document-intelligence-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Translator Name | Translator-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Open AI Name | Openai-<inject key="Deployment ID" enableCopy="false"></inject> |
    |Open AI Key | Paste the OpenAI key that you copied in task 1 |

      ![](./media/24-07-2024(35).png)

1. Leave other value as default and click on **Review + create** button, review the configuration, and click on **Create** button.

    ![](./media/24-07-2024(34).png)






    




