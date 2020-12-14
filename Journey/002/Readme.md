<!-- This template removes the micro tutorial for a quicker post and removes images for a full template check out the 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# SEC02-AZ100 — Create an Azure Policy

## Introduction

I chose this one because I needed to start somewhere and I figured I would start by completing all of the current challenges.  I had a busy today with taking the kids to see Grandpa so I needed something relatively light weight.

## Use Case

- Azure Policy is used to ensure that your Azure tenant is setup and operating the way that you have set by your standards.  You can use Azure Policy to enforce company standards and even standards that are enforce by other entities such as governments and 3rd parties.  HIPAA, NIST, PCI, FDIC are just a few.   You can set things in Azure Policy like enforcing what regions people can use or limiting types of resources.

## Cloud Research
![AzureBlueprint](.\CAFFoundation.jpg)
- I found that you can create multiple policies at once by using Azure Blueprints.  Since I already have the AZ-103 I figured I would try a new way to deply polices.
I created an Azure Blueprint in the tenant to use with my subscription.  I started with the CAF Foundation blueprint because it includes 10 policy assignments plus sets up Security Center.

![CAFFoundation](.\CAFFuondationArtifacts.jpg)

I went ahead and removed the Resource Groups that were there and created my own based off the Cloud Adoption Framework.  I added Shared Services for things like key vaults and Logs Analytics, Networks for vnets, Identity Services for Azure Active Directory Domain Services (AADDS), and First Application for the first Application (would probably use a better name if it wasn't a test.)

You can even add ARM templates to each of these Resource Groups and automate the deployment of things like AADDS or vnets.  I don't have enough time to go that far today though.

- What is Azure Policy?
    I already explained this above so I won't worry about this right now.
- What does the term scope refer to?
    Scope refers to the level that the policy will apply to.  It can be applied to a Management Group or Subscription and will apply to all child object inside.
- How many policy definitions can you have per scope?
    This is one that I did not know and definitely had to go look that up.  There is a limitation of 500 policy definitions per scope which seems like a ton.  I work mostly with small and medium size businesses so that seems like a lot.  500 on a small business seems like micromanaging, lol.  source: [Azure Policy Limitations](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#:~:text=There%27s%20a%20maximum%20count%20for%20each%20object%20type,management%20group%2C%20subscription%2C%20resource%20group%2C%20or%20individual%20resource.)
- What is an initiative definition?
    This is a group of policy definition that are usually grouped together because they are similar


## Social Proof

[Tweet](https://twitter.com/carlosmccray15/status/1338307156723044352)
