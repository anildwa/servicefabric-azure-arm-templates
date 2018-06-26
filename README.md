# servicefabric-azure-arm-templates
ARM templates for Service Fabric Deployment with various configuration options

## PreRequisits
---

### sf-slb-nsg-oms-pip.json
This template has the following configurations

- Multiple Node Type Loops using loop index. Use the loopCount parameter
- Enables Accelerated networking. Please refer to (this article)[https://docs.microsoft.com/en-us/azure/virtual-network/create-vm-accelerated-networking-cli]
- OMS workspace
- Nodetype with index 0 will not have public endpoints. The other node type will each have a public endpoint

