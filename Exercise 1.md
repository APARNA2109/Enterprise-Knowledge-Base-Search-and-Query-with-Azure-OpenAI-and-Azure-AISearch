# Exercise 1: Embedding creation


## Task 1: Deploy Azure OpenAI and Models

Azure OpenAI offers a web-based portal called **Azure OpenAI Studio** for deploying, managing, and exploring models. Follow these steps to deploy a model using Azure OpenAI Studio:

1. In the Azure portal, type **Azure OpenAI (1)** in the search box and select **Azure OpenAI (2)** from the results.

1. On **Azure AI Services | Azure OpenAI** blade, click **Create**.

   
1. Create an **Azure OpenAI** resource with the following settings:
   
    - **Subscription**: Default - Pre-assigned subscription.
    
    - **Resource group**: Select openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject> from drop-down
    
    - **Region**: Select **<inject key="Region" enableCopy="false" />**
    
    - **Name**: Openai-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard S0
  
1. Click **Review + Create** and then **Create**.
     

1. Once the deployment is complete, click **Go To Resources**.    


1. In the Azure OpenAI overview page, click **Go to Azure OpenAI Studio** to navigate to Azure AI Studio.



1. On the Welcome to Azure OpenAI Service page, click **Create new deployment**.

   

6. On the Deployments page, click **+ Create new deployment**.

   

7. In the Deploy model pop-up, enter the following details:
    

    - **Deployment name**: text-davinci-003

    - **Select a Model**: gpt-35-turbo-instruct
    
    - **Model version**: Auto-update to default
    
    - **Tokens per Minute Rate Limit (thousands)**: 40K

      
8. Click on the **Create** button to deploy a model that you will be playing around with as you proceed.

9. In the **Deployments** page, click on **+ Create new deployment**.

   

10. In the Deploy model pop-up, enter the following details:
    

    - **Deployment name**: text-embedding-ada-002

    - **Select a Model**: text-embedding-ada-002
    
    - **Model version**: 2(Default)
    
    - **Tokens per Minute Rate Limit (thousands)**: 40K
  

11. Click on the **Create** button to deploy a model that you will be playing around with as you proceed.


## Task 2: Create an Azure AI Search Resources

#### Creating AI Search service

1. In the Azure portal, type **AI Search (1)** in the search box and select **AI Search (2)** from the results.


1. On the **Azure AI services | AI Search** blade, click **Create**.

   
1. Create a **search service** resource with the following settings:
   
    - **Subscription**: Default - Pre-assigned subscription
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Aisearch-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard


1. Click **Review + Create** and then **Create**.
     

5. Once the deployment is complete, click **Go To Resources**.

6. On the overview page of the AI Search Search Service, copy the **URL** and store it in a notepad for future use.

7. In the AI Search blade, click on **Keys** under Settings, copy the Primary admin key, and store it in a notepad for future use.


    
#### Creating Document Intelligence

1. In the Azure portal, type **Document intelligence (1)** in the search box and select **Document intelligence (2)** from the results.


2. On the **Azure AI services | Document intelligence** blade, click **Create**.

    

3. Create a **Document intelligence** resource with the following settings:
   
    - **Subscription**: Default - Pre-assigned subscription.
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Document-intelligence-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard S0
    
    
4. Click **Review + Create** and then **Create**.

5. Once the deployment is complete, click **Go To Resources**.

6. In the Document intelligence resource, select **Key & Endpoint** from the left menu, click **Show Keys**, copy **KEY 1** and the **Endpoint**, and store them in a notepad for later use.

#### Creating Translator

1. In the Azure portal, type **Translator (1)** in the search box and select **Translator (2)** from the results.


2. On the **Azure AI services | Translator** blade, click **Create**.

    

1. Create a **Translator** resource with the following settings:
   
    - **Subscription**: Default - Pre-assigned subscription.
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Translator-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard S1
    
    
4. Click **Review + Create** and then **Create**.

5. Once the deployment is complete, click **Go To Resources**.

6. In the Translator resource, select **Key & Endpoint** from the left menu, click **Show Keys**, copy **KEY 1** and the **Endpoint**, and store them in a notepad for later use.


