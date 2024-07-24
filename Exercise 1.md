# Exercise 1: Embedding creation


## Task 1: Deploy Azure OpenAI and Models

Azure OpenAI offers a web-based portal called **Azure OpenAI Studio** for deploying, managing, and exploring models. Follow these steps to deploy a model using Azure OpenAI Studio:

1. In the Azure portal, type **Azure OpenAI (1)** in the search box and select **Azure OpenAI (2)** from the results.

1. On **Azure AI Services | Azure OpenAI** blade, click on **Create**.

   
1. Create an **Azure OpenAI** resource with the following settings and click on **Review + Create**:
   
    - **Subscription**: Default - Pre-assigned subscription.
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    - **Region**: Select **<inject key="Region" enableCopy="false" />**
    - **Name**: Openai-<inject key="Deployment ID" enableCopy="false"></inject>
    - **Pricing tier**: Standard S0
  
1. In the **Review + Create**, click on **Create**.
     

1. Once the deployment has succeeded, click on **Go To Resources**.      


3. In the Azure OpenAI overview page, click on **Go to Azure OpenAI Studio** it will navigate to **Azure AI Studio**.



5. On the **Welcome to Azure OpenAI Service** page, click on **Create new deployment**.

   

6. In the **Deployments** page, click on **+ Create new deployment**.

   

7. Within the **Deploy model** pop-up interface, enter the following details and then click on **Advanced options (3)**, followed by scaling down the **Tokens per Minute Rate Limit (thousands) (4)**:
    

    - **Deployment name**: text-davinci-003

    - **Select a Model**: gpt-35-turbo-instruct
    
    - **Model version**: Auto-update to default
    
    - **Tokens per Minute Rate Limit (thousands)**: 40K

      
8. Click on the **Create** button to deploy a model that you will be playing around with as you proceed.

9. In the **Deployments** page, click on **+ Create new deployment**.

   

10. Within the **Deploy model** pop-up interface, enter the following details and then click on **Advanced options (3)**, followed by scaling down the **Tokens per Minute Rate Limit (thousands) (4)**:
    

    - **Deployment name**: text-embedding-ada-002

    - **Select a Model**: text-embedding-ada-002
    
    - **Model version**: 2(Default)
    
    - **Tokens per Minute Rate Limit (thousands)**: 40K
  

11. Click on the **Create** button to deploy a model that you will be playing around with as you proceed.


## Task 2: Create an Azure AI Search Resources

#### Creating AI Search service

1. In the Azure portal, type **AI Search (1)** in the search box and select **AI Search (2)** from the results.


1. In the **Azure AI services | AI Search**, click on **Create**.

   
1. Create a **search service** resource with the following settings and click on **Review + Create**:
   
    - **Subscription**: Default - Pre-assigned subscription
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Aisearch-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard


1. In the **Review + Create**, click on **Create**.
     

1. Once the deployment has succeeded, click on **Go To Resources**.


1. On the overview page of the **AI Search** Search Service, copy the **Url** and paste the values on a Notepad. We will need this value in future exercises.

     
1. In the **AI Search**, click on **Keys** under Setting from the left menu, copy the **Primary admin key**, and paste the values it a Notepad we need this value in the future exercise.

    
#### Creating Document Intelligence

1. In the Azure portal, type **Document intelligence (1)** in the search box and select **Document intelligence (2)** from the results.


1. In the **Azure AI services | Document intelligence**, click on **Create**.

    

1. Create a **Document intelligence**, resource with the following settings and click on **Review + Create**:
   
    - **Subscription**: Default - Pre-assigned subscription.
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Document-intelligence-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard S0
    
    
1. In the **Review + Create**, click on **Create**.

    

1. Once the deployment has succeeded, click on **Go To Resources**.

       

1. In the Document intelligence resource on the **Azure Portal**, select **Key & Endpoint (1)** from the left menu, and click on **Show Keys (2)**. Copy the **KEY 1 (3)** and **Endpoint (4)**, and store them in a notepad for later use.


#### Creating Translator

1. In the Azure portal, type **Translator (1)** in the search box and select **Translator (2)** from the results.


1. In the **Azure AI services | Translator**, click on **Create**.

    

1. Create a **Translator**, resource with the following settings and click on **Review + Create**:
   
    - **Subscription**: Default - Pre-assigned subscription.
    
    - **Resource group**: openai-embedded-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Region**: Select <inject key="Region" enableCopy="false" />
    
    - **Name**: Translator-<inject key="Deployment ID" enableCopy="false"></inject>
    
    - **Pricing tier**: Standard S1
    
    
1. In the **Review + Create**, click on **Create**.

    

1. Once the deployment has succeeded, click on **Go To Resources**.


1. In the Translator resource on the **Azure Portal**, select **Key & Endpoint (1)** from the left menu, and click on **Show Keys (2)**. Copy the **KEY 1 (3)** and **Endpoint (4)**, and store them in a notepad for later use.


