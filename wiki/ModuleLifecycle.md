<h1 align="center"> Terraform - Module Lifecycle </h1>

# Index

- [Introduction](#introduction)
- [Modules Lifecyle Flow](#modules-lifecycle-flow)
    - [Terraform Framework Provides Solution?](#terraform-framework-provides-solution-?)
    - [Required Module is in Terraform Framework](#require-module-is-in-terraform-framework)
    - [There is not such module within terraform Framework](#there-is-not-such-module-within-terraform-framework)
        - [Terraform Framework Development Guidelines](#terraform-framework-development-guidelines)

# Introduction

The main objective of this section is to provide a clear guide, for everyone who works with Terraform, on how to proceed instead of going to a self-made approach.

It is important to have a clear understanding of the suggested methodology to ensure and enable an easy governance while keeping architects free of bureaucracy bottlenecks.

**In a general way, the Terraform framework methodology does not imply too much effort outside the project, but it implies a small alignment and avoiding misunderstandings.**

# Modules Lifecyle Flow

![Flow for a new module. Example with MSK from AWS.](https://github.com/LuisUrresti/GitHubWikiExample/blob/master/resources/terraform%20FWK%20flow.JPG)

**Quick Guide**

- Before launching yourself into a search for a new module, just check the Terraform FWK module list: AWS - Terraform Modules or Azure - Terraform Modules
- If you find a module that fits your needs, check if it is in its latest version accessing the original module's repository (update it if it's deprecated)
- If there isn't any module useful for your task, search for one in the Terraform Framework using the quality criteria defined in this page below.
- Once you find a module, fork it from its original repository in a new repository in the Everis - Technology & Advanced Solutions
- Only if there is no way to find such requirement (make sure you ask to other experts at this point) develop it by yourself following the Terraform Framework development guidelines.
                                       
                                THE NOTATION FOR EVERY MODULE REPOSITORY SHOULD BE THE FOLLOWING ONE

                                                    {provider}-{cloud}-{module}

                                                            for example:

                                                        terraform-aws-vpc

## Terraform Framework Provides Solution?

The first thing you have to do is to always ensure if the required module is already included in terraform FWK.

This can be checked here:

- AWS - Terraform Modules
- Azure - Terraform Modules

From here, you have two possibilities.

## Required Module is in Terraform Framework

If the module is already included in the Framework, go to its repository (via the [Everis - Technology & Advanced Solutions](https://github.com/everis-technology)) and check that Terraform Framework version is the latest available on the community.

If the framework module version is not its latest must **update it before using it!** Do this by **forking** the module's last version to the [Everis - Technology & Advanced Solutions](https://github.com/everis-technology) corresponding repository.

(Also, remember to put a comment in Jira to keep track of the performed actions).

## There is not such module within terraform Framework

1. Create an entrance in inventory so everybody can know that someone is working on that. Please add a JIRA so everybody can update actions related to that module and ensure traceability of actions within the FWK. (who choose it, reasons, problems while updating, and so on) 
2. Try to find a module in the community that can be included in framework. It's always interesting to check for a module in the "trusted creators" in the AWS - Terraform Modules#AWSTrustedModulesCreatorsList or the Azure - Terraform Modules#AzureTrustedModulesCreatorsList.
    - Once you have found a candidate module check the Terraform framework requirements.
        - Functionality offered by the module in terms of the component
        - Number of downloads. 
        - Repo Stars
        - Security Compliance Checks
        - Documentation
        - Examples
    - In the rare case that you find yourself unable to find a trusted module for your requirements and after asking other experts for a solution, you can develop the module by yourself. (Follow guidelines below) 
3. Document that module and (**after validating that it works as expected**) include it in framework:
    - Update modules list (AWS - Terraform Modules o Azure - Terraform Modules)
    - If needed update trusted modules creator list (AWS - Terraform Modules#AWSTrustedModulesCreatorsList o Azure - Terraform Modules#AzureTrustedModulesCreatorsList)
    - Create an example if not provided.
    - <u>Include it in a new [Everis - Technology & Advanced Solutions](https://github.com/everis-technology) repository by forking it from its original repository.</u>
4. Mark the Jira task as resolved, update it and use its last version within your project.

### Terraform Framework Development Guidelines

In case that there is not a module in the community that can provide you the functionality that you are looking for and you are going to develop your own module, we suggest some guidelines to make the module more reusable in order to add it to the framework.

The main objective is to make **highly configurable and reusable modules**. This can be achieved making the module accept multiple values and different options of configuration avoiding “hard-coding” arguments values and using optional variables or other data structures. 

In this repository (In the terraform-aws-modules-examples folder) can be found some examples of small modules that follow this guidelines: https://umane.everis.com/git/CCCPCP/terraform/terraform-framework.git. We will refer to these modules in order to give examples for the following guidelines:

1. **Optional variables:** One approach to do this is to contemplate different configurations by making parameters optional setting them by default to null and this way be able to use several configurations for the resources only giving a value to these variables. An example of this could be the in the module route53 the variable vpc_id, with a default value of null and which if it is specified will make the route53 zone private (by default will be public).
2. **Object map/list:** One interesting data structure that can help to make the modules more configurable is a map or list of objects. Two example of this are the private_subnets map defined in the module network, that will create as many private subnets as indicated in the map and with the given values, and the tables map defined in the dynamodb module, that allows to create the desired number of dynamodb tables with its attributes.
    - Optional objects: a very interesting experimental feature in terraform 0.14 is the possibility to define optional objects which if there are not specified will take null value. As it is an experimental feature, until a new terraform version is released, a terraform experiments block must be specified to use it. An example of this feature can be seen in the dynamodb module, in the definition of the tables variable (in variables.tf file).
3. **Examples:** A very helpful practice is to introduce an example of use in a folder named sample or example within the module which can be used to test it very quickly and to see how it works. Examples like this are in the sample folder of each module of the repository. The examples in the repository use terragrunt, a terrraform wrapper, to execute them you need to have terragrunt installed (and terraform of course), open a terminal in the sample module folder and type terragrunt plan or terragrunt apply.
4. **Documentation:** The modules will be self-documented via README files, as they are in the examples.

After developing a module, upload it to the [Everis - Technology & Advanced Solutions](https://github.com/everis-technology) corresponding repository using the specified notation.

