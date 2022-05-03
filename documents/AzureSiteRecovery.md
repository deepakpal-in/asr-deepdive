# Azure Site Recovery (ASR)

Azure Site Recovery is a service provided by Microsoft azure for the establish a reliable business continuity
and disaster recovery (BCDR) strategy that keeps your data safe, and your apps and workloads online, when planned and unplanned outages occur.

Site recovery helps by replicating the workloads from primary site to secondary/recovery site when an outage occurs at your primary site.

Handling the DC-DR of the Infrastructure using the Azure Site Recovery is a great option but this is a time consuming activity as well. Usually organizations wants to setup an automated DR functionality under their
business continuity planning to handle unexpected disaster timly and efficiently.

To achieve this kind of business requirements we can opt to go for the automation of Azure Site Recovery as a BCDR
solution for effective DR solution under the compliant RTO for the Infrastructure Services.

There are multiple ways using which this can be achieved. We will be focusing mainly on the automated Azure Site Recovery using the PowerShell/Azure PowerShell scripts.

## Considerations

* Azure has recomended few pair of the primary and recovery location. Prefere to use those pair to setup the DC-DR locations.
  * Refer to the official microsoft link for more information on [Azure Regional Pairing](https://docs.microsoft.com/en-in/azure/availability-zones/cross-region-replication-azure#azure-cross-region-replication-pairings-for-all-geographies)
* Choosing from the Azure regional pairs we are considering Central US as primary site and the East US 2 as the recovery site
* For a seamless recovery experience all of the recovered VMs will have same name and the same private IP address after recovery
* Public IPs are not handled in the scope of this project (this feature can be added in future) .
