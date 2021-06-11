<h1 align="center"> Terraform Framework </h1>

# Index

- [Introduction](#introduction)
- [Governance](#governance)
    - [Modules](#modules)
        - [Terraform Framework AWS Modules](#terraform-framework-aws-modules)
        - [Terraform Framework AWS Trusted Creators](#terraform-framework-aws-trusted-creators)
        - [Terraform Framework Azure Modules](#terraform-framework-azure-modules)
        - [Terraform Framework Azure Trustred Creators](#terraform-framework-azure-trusted-creators)
    - [BluePrints](#blueprints)
        - [Terraform Framework AWS BluePrints](#terraform-framework-aws-blueprints)
        - [Terraform Framework Azure BluePrints](#terraform-framework-aws-blueprints)
    - [Repository](#repository)

# Introduction

Terraform FWK is an initiative that aims:

1. Reusing terraform modules while working on projects.
2. To have an easy way to provision referenced architectures.

Although it is very common to use terraform within our projects, every time we need to provision an specific managed service, we use to invest and reuse several modules instead of creating a set of trusted modules chosen from available community options.

So the main idea here is to create a methodology of working with terraform that provide us a set of already tested modules that we can combine to implement our reference architectures blueprints. 

![Framework 1](https://github.com/LuisUrresti/GitHubWikiExample/blob/master/resources/fwk1.JPG)

Main benefits of this approach are:

- Every projects using terraform in the same way. 
- Changing between project simplified cause low level modules are the same.
- Efficiency in project implementation as modules have been already chosen by previous projects.
- Reusability and improved trust of proposed modules.
- Modules are evolved by community that is faster than us so we have to stay updated.
- Blueprints are an easy way to set up trusted architectures.

# Governance 

## Modules 

In Terraform Framework a module is a set of terraform configuration files that allow you to create a logical abstraction on the top of some resource set. In other words a module allow you to provision and configure a set of resources together that can be reused many times.

One simple example of a module could be: https://registry.terraform.io/modules/cloudposse/dynamodb/aws/latest

You can learn in depth in official documentation of Harsicorp: https://learn.hashicorp.com/tutorials/terraform/module

### Terraform Framework AWS Modules

The list of AWS modules in  framework:

    AWS - Terraform Modules

### Terraform Framework AWS Trusted Creators

The list of AWS modules creators that somehow have become essentials:

    AWS - Terraform Modules#AWSTrustedModulesCreatorsList

### Terraform Framework Azure Modules

The list of AWS modules in  framework:

    Azure - Terraform Modules

### Terraform Framework Azure Trusted Creators

The list of AWS modules creators that somehow have become essentials:

    Azure - Terraform Modules#AzureTrustedModulesCreatorsList

## BluePrints

In Terraform Framework a Blueprint is a recipe that uses different modules of Terraform Framework to deploy a set of resources, that group together provide specific functionality. 

We mainly aim here to create blueprints for specific reference architecture layers like Observability, Application runtime, DevOps for instance.

### Terraform Framework AWS Blueprints

    AWS - Terraform BluePrints

### Terraform Framework Azure Blueprints

    Azure - Terraform BluePrints

## Repository

All terraform FWK repositories are inside CCCPCP Steps gitlab group:

 https://umane.everis.com/git/CCCPCP/terraform


