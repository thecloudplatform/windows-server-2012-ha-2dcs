# Create 2 new Windows Server 2012 VMs, create a new AD Forest, Domain and 2 DCs in an availability set

This template will deploy 2 new VMs (along with a new VNet, Storage Account and Load Balancer) and create a new AD forest and domain, each VM will be created as a DC for the new domain and will be placed in an availability set. Each VM will also have an RDP endpoint added with a public load balanced IP address.

Added Network Security Group


Click the button below to deploy

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fthecloudplatform%2Fwindows-server-2012-ha-2dcs%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fthecloudplatform%2Fwindows-server-2012-ha-2dcs%2Fmaster%2Fazuredeploy.json" target="_blank">
    <img src="http://armviz.io/visualizebutton.png"/>
</a>

# Known Issues

+	This template is entirely serial due to some concurrency issues between the platform agent and the DSC extension which cause problems when multiple VM and\or extension resources are deployed concurrently, this will be fixed in the near future
