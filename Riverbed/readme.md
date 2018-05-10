The following POST request was used to create a new SD-WAN site:

https://18.221.166.135:7002/restconf/api/data/vpn-sp-riverbed:organizations

See: create_new_SD-WAN.xml

This will create a new site in an organization called “AWS-TMF-1” with a name of “LON” and will configure and deploy a virtual gateway on a virtual uCPE (running in the Azure environment) which has been registered in the SD-WAN orchestrator by the name “sdp-azure-cpe-1”.

For the purposes of the Catalyst demo, the names and locations of the site and organization are variable; the only data that cannot be chaged are the values for the bridges (as these are the binding points for the virtual gateway on the uCPE) and the policy (as this policy will allow all traffic between the SD WAN sites).

In a similar way we have also create a site a the Data Center end using this payload:

See: create_new_DC.xml


There are also additional APIs that have been implemented. For example, to fetch some operational data from the SD WAN orchestrator issue a GET request to:

https://18.221.166.135:7002/restconf/api/data/vpn-sp-riverbed:organizations/organization=AWS-TMF-1

(if a different organization name has been used then replace the name from “AWS-TMF-1” to your organization.)

There are also endpoints to support the deletion of a site or an organization. For example, to delete a site, issue a DELETE request to 

https://18.221.166.135:7002/restconf/api/data/vpn-sp-riverbed:organizations/organization=<Name of Org>/site=<node-id>,<site-name>

to delete an entire organization (including all it’s sites), issue a DELETE request to:

https://18.221.166.135:7002/restconf/api/data/vpn-sp-riverbed:organizations/organization=<Name of Org>
