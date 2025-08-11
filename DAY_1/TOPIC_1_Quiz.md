## **Scenario 1: The Over-Ambitious Retail AI**

**Background:**  
_BrightMart_, a national retail chain, wants to deploy a  **data-driven recommendation system**.  
The CIO insists on including:

-   Predictive analytics for customer buying habits
    
-   Real-time targeted marketing
    
-   Fraud detection
    
-   Automatic price adjustment based on competitor data
    

They have given the  **data science team**  4 months and a budget for only two new data engineers.

----------

**Q1:**  
As the lead data science practitioner, which  **TWO**  actions should you recommend  **first**  to prevent  **scope creep**  while aligning with  **design thinking principles**?

-   A. Reduce the project objectives to the most critical, high-value deliverables based on stakeholder consensus.
    
-   B. Hire temporary contractors to speed up delivery and meet all four original goals.
    
-   C. Identify the primary pain points through stakeholder workshops and customer empathy mapping.
    
-   D. Accept all four goals but extend the project timeline and budget by negotiating with management.
    

----------

**Q2:**  
During the initial stakeholder interviews, the marketing director demands access to  **all raw transactional data**  to "train her own model." The CIO objects due to  **data privacy regulations**. Which TWO governance and privacy considerations are most relevant here?

-   A. GDPR restrictions on personal data sharing
    
-   B. PCI DSS compliance for cardholder data
    
-   C. MVP testing procedures for stakeholder buy-in
    
-   D. Right to portability under open-data initiatives
    

----------

## **Scenario 2: The Banking Data Dilemma**

**Background:**  
_NorthBay Bank_  wants to improve loan approval accuracy. They have:

-   Customer demographics (**structured**  data in SQL)
    
-   Loan repayment histories (**semi-structured**  XML)
    
-   Call transcripts with customers (**unstructured**  audio, being transcribed to text)
    

They want a  **POC within 8 weeks**.

----------

**Q3:**  
Which  **TWO**  immediate actions will most effectively enable a  **feasible POC**  within time constraints?

-   A. Restrict initial data usage to the SQL and XML datasets only.
    
-   B. Include audio transcripts now to maximize feature diversity.
    
-   C. Focus on building an MVP model for classification (approve/deny) based on available structured/semi-structured data.
    
-   D. Implement a clustering model for loan segmentation first, then add classification later.
    

----------

**Q4:**  
A senior VP asks why the team can't "just add the audio data" since it "might improve accuracy." Your answer should emphasize:

-   A. ETL complexity and transformation time for unstructured data in the POC phase
    
-   B. GDPR compliance for recorded calls
    
-   C. The importance of clustering before classification
    
-   D. The need to democratize data access across all departments immediately
    

----------

## **Scenario 3: The Misaligned Metrics**

**Background:**  
_FitFast_, a fitness wearables company, launches a  **predictive maintenance**  system for its devices.  
KPIs include:

-   95% prediction accuracy for device failures
    
-   <2% false positive rate
    

However, customer satisfaction scores  **drop**  after launch.

----------

**Q5:**  
Which  **TWO**  likely oversights in  **project scoping**  or  **problem formulation**  could explain this?

-   A. Not including qualitative customer feedback in model evaluation
    
-   B. Using regression instead of classification for failure prediction
    
-   C. Not considering the business outcome of false positives on customer trust
    
-   D. Failing to collect sufficient historical device usage data
    

----------

**Q6:**  
If the team wants to improve both  **technical KPIs**  and  **customer satisfaction**, which stakeholder engagement step is MOST important?

-   A. Hosting cross-departmental review meetings to assess current KPIs in business terms
    
-   B. Adding more data sources immediately for better model accuracy
    
-   C. Performing advanced hyperparameter tuning to optimize recall and precision
    
-   D. Releasing the updated model to early adopters as an MVP for targeted feedback
