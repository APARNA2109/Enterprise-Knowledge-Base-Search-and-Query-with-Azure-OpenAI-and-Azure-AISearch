# Exercise 1: 

## Task 1: Create an Azure AI Search service

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

    
## Task 2: Create an Azure AI Search resource

#### Creating Document intelligence

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



     
