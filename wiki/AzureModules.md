<h1 align="center"> Terraform - Azure Modules </h1>

# Index 

- [Azure Modules List](#azure-modules-list)
- [Azure Trusted Modules Creators List ](#azure-trusted-modules-creators-list)

# Azure Modules List
| Module Name | Module Description | Community Repo | Everis Repo | Last Version in Framework | Related Issue |
| :--------:  | :----------------: | :------------: | :---------: | :-----------------------: | :-----------: |
| ACI | Module for Azure Container Instances  | [aci](https://github.com/claranet/terraform-azurerm-aci) | [aci](https://github.com/everis-technology/terraform-azurerm-aci) | v4.0.0 | - |
| ACR | Azure Container Registry Service | - | [acr](https://github.com/everis-technology/celz-terraform-azure-acr.git) | - | - |
| AKS | Azure Kubernetes Service | - | [aks](https://github.com/everis-technology/celz-terraform-azure-aks) | - | - |
| App Service | Module ofr Azure App Service (Web App) | - | [webapp](https://github.com/everis-technology/celz-terraform-azure-webapp) | - | - |
| Application Insights | Module for Application Insights | [app-insights](https://github.com/bytejunkie/terraform-azurerm-application-insights.git) | [app-insights](https://github.com/everis-technology/terraform-azurerm-application-insights) | v1.0.0 | - |
| Application Gateway | Module for deploy an Application Gateway | - | [app-gateway](https://github.com/everis-technology/celz-terraform-azure-application-gateway) | - | - |
| Azure Function | Module for Azure Function | - | [functionapp](https://github.com/everis-technology/celz-terraform-azure-functionapp) | - | - |
| Azure Redis Cache | Module for Azure Cache for Redis. | [redis](https://github.com/claranet/terraform-azurerm-redis) | [redis](https://github.com/everis-technology/terraform-azurerm-redis) | v4.0.0 | - |
| Key Vault | Key Vault | - | [keyvault](https://github.com/everis-technology/celz-terraform-azure-keyvault.git) | - | - |
| Load Balancer | Module for Azure Load Balancer | [loadbalancer](https://github.com/Azure/terraform-azurerm-loadbalancer) | - | v3.2.0 | - |
| Log Analytics Workspace | Module for Log Analytics workspace | - | [log-analytics](https://github.com/everis-technology/celz-terraform-azure-log-analytics-workspace.git) | - | - |
| Management Groups | Management Groups | 	[magement-groups](https://github.com/terraform-azurerm-modules/terraform-azurerm-management-groups) | [magement-groups](https://github.com/everis-technology/terraform-azurerm-management-groups)| v0.2.20 | [Management Group Issue](https://github.com/LuisUrresti/GitHubWikiExample/issues/1) |
| Monitor Diagnostic Setting | Module for setting the diagnostic configuration | - | [diagnostics](https://github.com/everis-technology/celz-terraform-azure-diagnostic-settings) | - | - |
| MySQL | Module for Azure MySQL server | [mysql](https://github.com/claranet/terraform-azurerm-db-mysql) | [mysql](https://github.com/everis-technology/terraform-azurerm-db-mysql) | v4.1.1 | - |
| Network Peering | Module for Network Peering	 | [peering](https://github.com/scalair/terraform-azure-vnet-peering) | [peering](https://github.com/everis-technology/terraform-azure-vnet-peering) | v2.0.0 | [Network Peering Issue](https://github.com/LuisUrresti/GitHubWikiExample/issues/2) |
| NSG | Module for Network Security Group | [nsg](https://github.com/Azure/terraform-azurerm-network-security-group) | [nsg](https://github.com/everis-technology/terraform-azurerm-network-security-group) | v3.5.0 | - |
| PostgreSQL | Module for PostgreSQL single server | 	[postgresql](https://github.com/Azure/terraform-azurerm-postgresql) | [postgresql](https://github.com/everis-technology/terraform-azurerm-postgresql) | v2.1.0 | - |
| PostgreSQL Flexible Server | Module for PostgreSQL flexible server | - | - | - | - |
| Private Endpoint | Module for Private Endpoint | - | - | - | - |
| Resource Group | Module for Resource Group | - | [rsg](https://github.com/everis-technology/celz-terraform-azure-resource-group) | - | - |
| Storage Account | Module for Storage Account | - | [storage-account](https://github.com/everis-technology/celz-terraform-azure-storage-account) | - | - |
| VNET + NSG + UDR | Virtual Network, Network Security Group and User Defined Route | - | [vnet](https://github.com/everis-technology/celz-terraform-azure-vnet) + [udr](https://github.com/everis-technology/celz-terraform-azure-vnet) | - | - |
| VPN | Module for Virtual Network Gateway | [vpn-gateway](https://github.com/kumarvna/terraform-azurerm-vpn-gateway) | [vpn-gateway](https://github.com/everis-technology/terraform-azurerm-vpn-gateway) | v1.0.0 | - |

# Azure Trusted Modules Creators List
| Trusted Creator Name | Description | Organization Repo | Comments |
| :-----------------:  | :---------: | :---------------: | :------: |
| Terraform Azure Modules | Official Azure Terraform modules | [Terraform Azure Modules](https://github.com/terraform-azurerm-modules) | |
| Microsoft Azure | APIs, SDKs and open source projects from Microsoft Azure | [Microsoft Azure](https://github.com/Azure?q=terraform-azurerm&type=&language=&sort=) | |
| Celz | Collection of Terraform Azure modules created by Everis - Technology & Advanced Solutions | [Everis](https://github.com/everis-technology) | |
| Claranet | Open sourced projects from and contributed-to by Claranet. | [Claranet](https://github.com/claranet) | They force to use their own naming conventions with several variables like client_name and location_short in all their repos. This can be either changed or used like this if it is consider appropriate.| 
| Scalair | Scalair is a Public and private cloud operator. | [Scalair](https://github.com/scalair) | This creator has been selected to bring the Network Peering Terraform module. Microsoft Azure creator has linked a repository for this module, but it is not up to date (2018). |
| Kumaraswamy Vithanala | Kumarvna is his own repository | [Kumaraswamy](https://github.com/kumarvna) | This repository has been selected for the Virtual Network Gateway module. It is the best one that has been found in the comunity. |
| Matt Short | Bytejunkie is his own repository | [Bytejunkie](https://github.com/bytejunkie) | This repository has been selected for the Application Insight module. |
