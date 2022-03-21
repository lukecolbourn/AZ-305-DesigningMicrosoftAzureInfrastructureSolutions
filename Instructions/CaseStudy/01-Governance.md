---
casestudy:
    title: 'Design a governance solution'
    module: 'Governance solutions'
---

# Design a governance solution

Estimated time: 90 minutes

## Requirements

Tailwind Traders is planning on making some significant changes to their governance solution. They have asked for your assistance with recommendations and questions. Here are the specific requirements.

* **Cost and accounting**. Tailwind Traders has two main business units that handle Apparel and Sporting Goods. Each of the business units consist of three departments: Product Development, Marketing, and Sales. Each business unit and subunit will be responsible for tracking their Azure spend. At the same time, the Enterprise IT team will be responsible for providing company-wide Azure cost reporting.

* **New development project**. The company has a new development project for customer feedback. The CFO wants to ensure all costs associated with the project are captured. For the testing phase, workloads should be hosted on lower cost virtual machines. The virtual machines should be named to indicate they are part of the project. Any instances of non-compliance with resource consistency rules should be automatically identified.

## Tasks

1. **Cost and accounting** 

    * What are different ways Tailwind Traders could organize their subscriptions and management groups. Which would be the best to meet their requirements? 

    * Design two alternative hierarchies and explain your decision-making process.

2. **New development project** 

    * What are the different ways Tailwind Traders could track costs for the new development project?
    * How are you ensuring compliance with the requirements for virtual machine sizing and naming? 
    * Propose at least two ways of meeting the requirements. Explain your final decision. 

How are you incorporating the Well Architected Framework pillars to produce a high quality, stable, and efficient cloud architecture?

## Answers

1. **Cost and accounting**
![image](https://user-images.githubusercontent.com/6578121/159335341-d53a71d9-5187-4dac-bd1e-51c0d80789cf.png)
![image](https://user-images.githubusercontent.com/6578121/159334853-695ce709-4a9c-418c-a123-f763e7921dfa.png)


2. **New development project** 

    * Tag new project resources with a project key/identifier, and pull cost reports by tag.
    * and/or, deploy the new projects resources in their own resource group(s), and produce cost reporting by resource group.
    * Create prod and non-prod, subscriptions under the new projects business unit.
    * Create 2 Azure policies, one for VM max size and one defining naming convention.
    * Apply VM size policy to non-prod new project resource groups.
    * Apply naming convention policy to all new project resource groups.
