# Cafe Supremo Supplier Portal Solution

This solution automates  many of the steps in the procurement process using Oracle Integration Cloud to coordinate actions between the buyer using JD Edwards order management system and the supplier using folders, files, conversations, and a web interface provided in Oracle Content and Experience Cloud.  

## Getting Started

Use the resources provided with this integration example as a starting point to create your own solution.

### Documentation

For detailed information about setting up and using the solutions, see [Understanding the Supplier Portal Integration](https://www.oracle.com/pls/topic/lookup?ctx=en/cloud/paas/content-cloud/solutions&id=CECSI-GUID-8C4C5340-8248-4F72-AF6E-64F78F6D234C) in _Creating Solutions with Oracle Content and Experience Cloud_.

### Integrated Services

The supplier portal solution presented here uses the integration features of the following cloud services to provide a coherent procurement process flow for both buyer and supplier.

| Service | Description |
| ------------- | ------------- |
| JD Edwards EnterpriseOne | Using processes created with JD Edwards Orchestrator, the supplier portal solution augments JD Edwards order management system to send purchase orders, receive invoices, and manage notifications and status updates between the integrated services. The supplier portal solution requires JD Edwards Tools release 9.2.2. |
| Oracle Content and Experience Cloud | Designated folders are the repository for purchase orders, invoices and receipts for each supplier. Suppliers sign in to a website to get real-time access to the documents based on their status and to perform their tasks in the procurement process. |
| Oracle Process Cloud Service | The process coordination between order management, document repository, and web portal is handled by processes defined in Oracle Process Cloud Service. |
| Oracle Integration Cloud Service | All of the integrations used by Oracle Process Cloud Service are hosted and managed in Oracle Integration Cloud Service. |

### Basic Steps

To set up and use the supplier portal solution:

1. Make sure you have access to the services listed above.

2. Download the source code listed below.

3. Define users and assign roles for the process participants. 

4. You must set up the integration between JD Edwards and Oracle Content and Experience Cloud. 

5. Install the JD Edwards EnterpriseOne Orchestrator studio (version 6.0.2 and above) and the orchestrations used in the solution. Individual orchestrations may have additional setup requirements. 

6. You must install, configure, and deploy the application used by Oracle Process Cloud Service.

7. You must install the process integrations in Oracle Integration Cloud Service and configure the required connections. 

8. You must create the folder hierarchy in Oracle Content and Experience Cloud, specify the appropriate access permissions, and define the metadata collections associated with folders. 

9. You must configure integration settings in Oracle Process Cloud Service and Oracle Content and Experience Cloud before users can take advantage of the integrated functionality.

10. You must import the supplier portal template, then create and configure a new site from the template. 

11. Use the solution to verify that it works correctly. 


## Source Code

This repository provides the  following code samples for this solution.

| Name | Description |
| ------------- | ------------- |
| Supplier Portal.exp | Contains the application used with Oracle Process Cloud Service. |
| JDESupplierPortalIntegrations.par | Contains all integrations called by the Oracle Process Cloud Service application. |
| CafeSupremoSuppliersPortal.zip | Contains the website template which includes all the site pages and functionality required to create the supplier portal website. |
| P2P\_Orchestration\_Samples\_26_99.par | Contains all JD Edwards orchestrations and notifications used by the supplier portal. |
| Sample_Invoice.pdf | A sample supplier invoice document.   |

You must also download and install **JN14931.exe** under [bug 27360725](https://www.oracle.com/pls/topic/lookup?ctx=en/cloud/paas/content-cloud/solutions&id=jde-bug-27360725) from the JD Edwards update center.

This file contains versions of the following objects used in the supplier portal:  

* Purchase Order Print (R43500)

* Purchase Receiver Print (R43510)
  
## Disclaimer

All sample code is provided by Oracle for illustrative purposes only. The objective of this sample is only to demonstrate one possible supplier portal solution using services and may not represent other best practices, whether functional or technical. This sample code has not been thoroughly tested under all conditions. Oracle, therefore, cannot guarantee or imply security, reliability, serviceability, or function of the sample code. All sample code contained herein are provided to you AS IS without any warranties of any kind. The implied warranties of non-infringement, merchantability and fitness for a particular purpose are expressly disclaimed.