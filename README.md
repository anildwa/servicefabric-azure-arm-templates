# servicefabric-azure-arm-templates
ARM templates for Service Fabric Deployment with various configuration options

## PreRequisites

* Azure Key Vault in the same region where the Service Fabric Cluster would be created.
* Client Authentication Certificate - either self signed or issued from a Trusted Root CA.
* Azure Virtual Network with sufficient address space to provision VMs
* S2S VPN/Express Route Connection or a Jump Box VM in the existing VNet
* Azure CLI installed on Windows, Mac OS or Linux machine. 
* Service Fabric CLI SFCTL installed on Windows, Mac OS or Linux machine.
* Access to Azure Subscription

## sf-slb-nsg-oms-pip.json
This template has the following configurations


- Multiple Node Type Loops using loop index. Use the loopCount parameter
- Enables Accelerated networking. Please refer to [this](https://docs.microsoft.com/en-us/azure/virtual-network/create-vm-accelerated-networking-cli)
- OMS workspace
- Nodetype with index 0 will not have public endpoints. The other node type will each have a public endpoint

