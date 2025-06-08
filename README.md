# Azure Logic App Integration for EDL Manager IP Blocklist

This repository provides an Azure Logic App template designed to add IP addresses to an EDL (External Dynamic List) [Manager Blocklist](https://edlmanager.com/). This Logic App integration is compatible with any firewall solution that supports EDLs.

## Requirements

### Prerequisites

EDL Manager API Key: Obtain your API Key from EDL Manager by following the steps detailed: [How Top Obtain API Key](https://support.edlmanager.com/support/solutions/articles/70000636857-edl-manager-api).

Manual EDL Source: Create a Manual EDL Source in EDL Manager following instructions: [Create a Manual EDL Soruce](https://support.edlmanager.com/support/solutions/articles/70000368734-custom-sources).

Manual Source ID: Retrieve the Manual Source ID by logging into the EDL Manager portal and navigating to: [Manual Source](https://edlmanager.com/api/v1/sources/manual)

## Azure Permissions

Ensure you have sufficient rights in Azure to create the following resources:

#### Azure Key Vault

#### Azure Logic Apps

#### Microsoft Sentinel

## Setup Instructions

Deploy the Logic App template provided in this repository.

Once deployment is complete, navigate to the Azure portal:

1. Go to your created Logic App.

2. Select API Connections.

3. Choose the Microsoft Sentinel API connection and click Edit.

Click Authorize, follow the authorization prompts, then click Save.

![image](https://github.com/user-attachments/assets/d7ce6a15-3d3f-493e-9124-a7e600e31a72)


# Usage

You can now trigger this Logic App as a playbook within Microsoft Sentinel to automatically block IP addresses. This automation integrates seamlessly with firewall solutions supporting dynamic EDL lists, ensuring timely and effective management of IP-based threats.

# Notes
When entering the API key into the Template, make sure that you start the key with Api-Key then the API Key EX Api-Key Zdl5P1Cu.ZCHu0AmO7ppQepsL4b8FnHflffUBYFV5. If you miss this step the API Key will fail. You can schedule this to run as a playbook. 
