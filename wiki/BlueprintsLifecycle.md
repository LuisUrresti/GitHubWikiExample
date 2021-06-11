<h1 align="center"> Terraform - BluePrints Lifecycle </h1>

# Index

- [Introduction](#introduction)
- [What is a Blueprint?](#what-is-a-blueprint-?)
- [Blueprint Lifecyle Flow](#blueprint-lifecycle-flow)
    - [Terraform Framework Provides Blueprints Solution?](#terraform-framework-provides-solution-?)
    - [Foreach module needed in blueprint](#foreach-module-needed-in-blueprint)


# Introduction

Main objective of this section is to provide a clear guide, for everyone working with terraform, on how to proceed when using a blueprint of the terraform Framework.

It's important to have a clear understanding of the methodology suggested to ensure and enable easy governance while keeping architects free of bureaucracy bottlenecks.

Overall, Terraform framework methodology does not imply too much effort outside the project, but it implies alignment and avoiding misunderstanding.

# What is a Blueprint?

A blueprint is a set of terraform modules grouped in a way in which they can be provided as an specific architecture solution for a customer business case.

A common blueprint example could be a set of different modules (MSK, EKS, S3, ...) that represent a generic observability solution based on a microservice application.

![Figure 1 - Example of blueprint providing observabilty (marked with red square) over a set of data](https://github.com/LuisUrresti/GitHubWikiExample/blob/master/resources/MicrosoftTeams-image.png)

# Blueprint Lifecycle Flow

![Figure 2 - Blueprint creation flow. Example with Observability System over AWS](https://github.com/LuisUrresti/GitHubWikiExample/blob/master/resources/blueprint-flow.png)

This flow represents the way in which you must proceed when you need a specific blueprint. 

**Quic Guide:**

- Before you start building an architecture solution, first check the terraform FWK blueprint list: AWS - Terraform BluePrints or Azure - Terraform BluePrints
- If you find one, do not reinvent the wheel. Just ensure all modules within the blueprint are in their last version (if not, update every module that is required) and use the blueprint with the last version of the specified modules.
- If there is no such blueprint, you will need to do it yourself, **BUT do not forget to add your blueprint to the FWK at the end of the project!**
- For each module needed:
    1. Try to use the Terraform FWK trusted modules looking into: AWS - Terraform Modules or Azure - Terraform Modules
    2. Try to find a community module as specified in Terraform - Module Lifecycle#ThereisnotsuchmodulewithinterraformFramework. Perform a guided search taking into account quality criteria for the Terraform Framework
    3. Only if there is no way to find a required module (**make sure you ask to other experts at this point**) develop it by yourself following the Terraform Framework development guidelines.

## Terraform Framework Provides Blueprints Solution?

The first thing you should do is to ensure if the required blueprint is already included in the Terraform FWK.

Check here:

- AWS - Terraform BluePrints
- Azure - Terraform BluePrints

If there isn't any blueprint that suits for that purpose or any that can be reused, then do it within your project but always following the Terraform FWK methodology so that you can include that blueprint in the Terraform FWK blueprints.

## Foreach module needed in blueprint

Follow the corresponding flow of the Terraform FWK modules: [Terraform - Module Lifecycle](ModuleLifecycle)
