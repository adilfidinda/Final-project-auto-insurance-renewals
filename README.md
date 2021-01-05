# Predicting Automobile Insurance Renewal
![alt text](https://decoratex.biz/bsn/fr/static/img/a/42515/466437/77586.jpg)

## Business Background
Automobile Insurance provides financial protection against vehicle's physical damage and bodily injury (include medical payment) due to traffic collisions and other incidents such as theft, fire, flood or falling objects on vehicles.

## Problem
The company wants to offer renewal insurance to customers. However, contacting all customers will certainly cost more so it is necessary to predict which customer will be contacted and agree to renew the insurance. In addition, keeping customers subscribed to insurance for a long time is more effective than finding new customers.

## Goals
- Reducing communication costs
- Retaining customers who take auto insurance services to remain customers
- Build a model to predict customer interest in renewal of vehicle insurance so it can help companies plan their communication strategies.

## Conclusion
- Only ~ 14% of customers agree to renewal
- More customers respond yes to basic coverage
    - it's enough to cover the basics when an accident occurs. It also cheaper then others coverage so it fits the customer's basic needs and budget.
- More than 50% of yes responses come from customers who have jobs
    - they have income that can be used to pay premiums. And there are also some jobs that require car insurance, for example drivers who have a higher risk while driving.
- More customers from suburbs who responded yes
- Personal auto policy is the most renewal type of policy
    - means this type of policy is in accordance with the needs of most customers in this company. Most customers own private cars and not cars used for business or customers are not registered with federal medicaid with hospitalization. This personal policy usually guarantees the owner of the vehicle and one or two close family members.
- Offer 1 and offer 2 are more attractive / valuable for customers
- Customers who have employment and any marital status, especially married, are more interested in renewals
- People whose last education are high school or below have a higher risk of driving so they will make more claims. According to the demographic basis, highly educated people tend to be responsible drivers. https://www.carinsurance101.com/does-my-education-level-affect-my-car-insurance/
- Oregon and Arizona customers who respond to yes have CLV almost on average so that these two states are potential for company revenue.
- Low income customers are more interested in renewal when an offer is offered 1
- High income customers are more interested in renewal when an offer is offered 2
- Customers tend not to be interested in offers 3 and 4 so that these offers are not valuable according to customers
- Each Renew Offer Type has different customer characteristics

## Recommendation
- **If you want to contact a customer, prioritize the following characteristics:**
    - People who are married and / or already working have a higher chance of meeting bills. They also have greater financial security than single customers or unemployed customers because they can accumulate assets. When you are married, of course, financial problems need to be considered. So, married customers tend to want to reduce the cost burden and protect their assets, one of which is their vehicle in the event of an accident, loss or theft, flood damage and others so that they do not interfere with other needs. https://cover.com/blog/car-insurance-married-vs-single/#:~:text=To%20insurers%2C%20the%20existence%20of,able%20to%20pool%20their%20assets.
    - Customers with basic coverage because in the United States, in some states, it is mandatory to have vehicle insurance at least for body injury and property damage so that it is sufficient to cover the basics when an accident occurs. Premium payment is cheaper so that it fits the customer's basic needs and budget.
    - Personal Auto Policy, which is this type of policy according to the needs of most customers in the company. Most customers own private cars and not cars used for business or customers are not registered with federal medicaid with hospitalization. This personal policy usually guarantees the owner of the vehicle and one or two close family members.
    - Customers with a higher education level are more likely to be responsible drivers so they will have a lower claim rate
    - Customers in suburbs because they have an average CLV above the average value which means the potential for company revenue because it can play a big role in the company's business activities.
    
- **Provide targeted types of offers to customers**

  a. Based on Vehicle Class and Size
    - Offer 1 : Four-Door Car (Large), Luxury Car (Small), Luxury SUV (Med), SUV (Large, Med, Small), Sport Car (Large)
    - Offer 2 : Four-Door Car (Large, Med, Small), Luxury Car (Med), Luxury SUV (Small), SUV (Large, Small), Sport Car (Med), Two-Door Car (Large, Med, Small)
    
  b. Based on Employment Status
    - Offer 1 : Disabled, Medical Leave, Retired, Unemployed
    - Offer 2 : Employed
    
  c. Based in Income Group
    - Offer 1 : Low Income
    - Offer 2 : Medium dan High Income
    
  d. Based on Coverage
    - Offer 1 : Premium
    - Offer 2 : Basic, Extended
    
  e. Based on premium
    - Offer 1 : Premi 85 - 150 dollar (Medium Premium) dan more than 150 dollar (High Premium)
    - Offer 2 : Premi 0 - 85 (Low Premium)    
    
- **Offers 3 and 4 can be removed from the policy for renewal offers because they are not valuable in terms of customer response**
- **Customers who are not interested in renewal, ask the reason**
    - If they have financial problem, it can be offered to reduce the type of coverage (from premium to basic) or level of policy (personal level 2 to personal level 1)
    - If the car is not with the customer (sold), you can periodically call back when the customer has bought a new car (especially for high income customers because it will be more possible to buy a car due to financial security)
- **Customers who are not interested in renewal**
    - If the company is integrated with a bank: it can be contacted again after an update of the bio, for example a customer who is unemployed has got a job so that it is more potential to receive insurance because it already has income and offers based on the appropriate offer
    - If the company is stand alone: it can be contacted periodically, customers who potential to make premium payments smoothly, for example Employed or medium-high income customers
  
## Machine Learning
<img src = "evaluation.JPG"/>
FN is the number of customers who are predicted not to be interested in renewal, even though they are actually interested, which can lead company to losing the opportunity to retain customers. FP is the number of customers who are predicted to be interested even though they are not actually interested which results in the company spending more communication costs. To optimize these two conditions, the most optimal FN and FP values of all models are needed so that the selected model is Support Vector Regression with Smote.
