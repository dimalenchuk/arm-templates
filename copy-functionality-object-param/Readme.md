This templates support creating **N-NodeType ServiceFabric cluster**.

Each NodeType has the following resources associated to it.
- Public IP Address Resource
- Load Balancer Resource
- Virtual Network Subnet

The template makes use of the following features
- [Object Parameter Input to Arm Template](https://docs.microsoft.com/en-us/azure/architecture/building-blocks/extending-templates/objects-as-parameters)
- [Copy Function Resource Iteration](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-multiple#resource-iteration)
- [Copy function Property Iteration](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-multiple#property-iteration)
- [Depends on Resource Iteration](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-create-multiple#depend-on-resources-in-a-loop)

