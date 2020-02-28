---

copyright:
  years: 2019, 2020

lastupdated: "2020-02-28"

keywords: vpc event, vpc activity tracker, vpc logdna

subcollection: vpc-on-classic

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:download: .download}


# Activity Tracker with LogDNA events
{: #at-events}

Use the {{site.data.keyword.at_full}} service to track how your users and applications interact with the {{site.data.keyword.cloud}} Virtual Private Cloud (VPC) in the {{site.data.keyword.cloud}}.
{:shortdesc}

The {{site.data.keyword.at_full}} service records user-initiated activities to change the state of a service in the {{site.data.keyword.cloud}}. For more information, see [{{site.data.keyword.at_full}}](/docs/Activity-Tracker-with-LogDNA?topic=logdnaat-getting-started#getting-started).

## List of events: Network resources
{: #events-volumes}

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| vpc  | is.vpc.vpc.create   | VPC was created  |
| vpc  | is.vpc.vpc.update   | VPC was updated  |
| vpc  | is.vpc.vpc.delete   | VPC was deleted  |
| vpc  | is.vpc.address-prefix.create  | Address Prefix was added to VPC  |
| vpc  | is.vpc.address-prefix.update  | VPC Address Prefix was updated  |
| vpc  | is.vpc.address-prefix.delete  | Address Prefix was removed from VPC  |
| vpc  | is.vpc.vpc-route.create   | Route was added to VPC   |
| vpc  | is.vpc.vpc-route.update   | VPC Route was updated  |
| vpc  | is.vpc.vpc-route.delete   | Route was removed from VPC   |
| floating-ip  | is.floating-ip.floating-ip.delete   | Floating IP was created  |
| floating-ip  | is.floating-ip.floating-ip.delete   | Floating IP was updated  |
| floating-ip  | is.floating-ip.floating-ip.delete   | Floating IP was deleted  |
| network-acl  | is.network-acl.network-acl.create   | Network ACL was created  |
| network-acl  | is.network-acl.network-acl.update   | Network ACL was updated  |
| network-acl  | is.network-acl.network-acl.delete   | Network ACL was deleted  |
| network-acl  | is.network-acl.rule.create  | Rule was added to Network ACL  |
| network-acl  | is.network-acl.rule.update  | Network ACL Rule was updated  |
| network-acl  | is.network-acl.rule.delete  | Rule was removed from Network ACL  |
| public-gateway | is.public-gateway.public-gateway.create   | Public Gateway was created   |
| public-gateway | is.public-gateway.public-gateway.update   | Public Gateway was updated   |
| public-gateway | is.public-gateway.public-gateway.delete   | Public Gateway was deleted   |
| security-group | is.security-group.security-group.create   | Security Group was created   |
| security-group | is.security-group.security-group.delete   | Security Group was deleted   |
| security-group | is.security-group.security-group.update   | Security Group was updated   |
| security-group | is.security-group.security-group-rule.create  | Rule was added to Security Group  |
| security-group | is.security-group.security-group-rule.delete  | Rule was removed from Security Group  |
| security-group | is.security-group.security-group-rule.update  | Security Group Rule was updated  |
| security-group | is.security-group.security-group-interface.attach | Interface was attached to Security Group   |
| security-group | is.security-group.security-group-interface.detach | Interface was removed from Security Group  |
| subnet   | is.subnet.subnet.create   | Subnet was created   |
| subnet   | is.subnet.subnet.update   | Subnet was updated   |
| subnet   | is.subnet.subnet.delete   | Subnet was deleted  |
| subnet   | is.subnet.network-acl.update  | Subnet's Network ACL was replaced   |
| subnet   | is.subnet.public-gateway.operate  | Public Gateway was attached to Subnet  |
| subnet   | is.subnet.public-gateway.operate  | Public Gateway was detached from Subnet  |

## List of events: Compute resources
{: #events-computes}

The following table lists the actions related to compute resources and the generation of events.

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| instance   | is.instance.instance.create   | Instance was created   |
| instance   | is.instance.instance.delete   | Instance was deleted   |
| instance   | is.instance.instance.update   | Instance was updated   |
| instance | is.instance.instance.start | Instance was started |
| instance | is.instance.instance.stop | Instance was stopped |
| instance | is.instance.instance.reboot | Instance was rebooted |
| instance   | is.instance.action.create   | Instance action was created  |
| instance   | is.instance.action.delete   | Pending instance action was deleted  |
| instance   | is.instance.network-interface_floating-ip.create | Floating ip was associated to instance network interface  |
| instance   | is.instance.network-interface_floating-ip.delete | Floating ip was Disassociated from instance network interface |
| instance   | is.instance.volume-attachement.create  | Instance volume attachment was created  |
| instance   | is.instance.volume-attachement.delete  | Instance volume attachment was deleted  |
| instance   | is.instance.volume-attachement.update  | Instance volume attachment was updated  |
| key  | is.key.key.create   | Key was created  |
| key  | is.key.key.delete   | Key was deleted  |
| key  | is.key.key.update   | Key was updated  |

## List of events: Image resources
{: #events-images}

The following table lists the actions related to image resources and the generation of events.

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| image  | is.image.image.create   | Image was created |
| image  | is.image.image.delete   | Image was deleted |
| image  | is.image.image.update   | Image was updated  |

## List of events: Storage resources
{: #events-storage}

The following table lists the actions related to storage resources and the generation an events.

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| volume  | is.volume.volume.create  | Volume was created  |
| volume  | is.volume.volume.update  | Volume was updated |
| volume  | is.volume.volume.delete  | Volume was deleted  |


## List of events: Load balancers
{: #events-load-balancers}

The following table lists the actions related to load balancers and the generation of events.

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| Load balancer |  is.load-balancer.load-balancer.create | Load balancer was created |
| Load balancer |  is.load-balancer.load-balancer.update | Load balancer was updated |
| Load balancer |  is.load-balancer.load-balancer.delete | Load balancer was deleted |
| Listener |  is.load-balancer.load-balancer.listener.create | Listener was created |
| Listener |  is.load-balancer.load-balancer.listener.update | Listener was updated |
| Listener |  is.load-balancer.load-balancer.listener.delete | Listener was deleted |
| Pool |  is.load-balancer.load-balancer.pool.create | Pool was created |
| Pool |  is.load-balancer.load-balancer.pool.update | Pool was updated |
| Pool |  is.load-balancer.load-balancer.pool.delete | Pool was deleted |
| Member |  is.load-balancer.load-balancer.pool.member.create | Member was created |
| Member |  is.load-balancer.load-balancer.pool.member.update | Member was updated |
| Member |  is.load-balancer.load-balancer.pool.member.delete | Member was deleted |
| Policy |  is.load-balancer.load-balancer.listener.policy.create | Policy was created |
| Policy |  is.load-balancer.load-balancer.listener.policy.update | Policy was updated |
| Policy |  is.load-balancer.load-balancer.listener.policy.delete | Policy was deleted |
| Rule |  is.load-balancer.load-balancer.listener.policy.rule.create | Rule was created |
| Rule |  is.load-balancer.load-balancer.listener.policy.rule.update | Rule was updated |
| Rule |  is.load-balancer.load-balancer.listener.policy.rule.delete | Rule was deleted |

Load balancer auditing events are recorded to {{site.data.keyword.at_full}} in the `us-south` region. The region in which you provision the load balancer service does not matter.
{:note}

## List of events: VPNs
{: #events-vpn}

The following table lists the actions related to VPNs and the generation of events.

| Resource  | Action  | Description  |
|:----------------|:-----------------------|:-----------------------|
| vpn  | is.vpn.vpn-gateway.create   | VPN Gateway was created |
| vpn  | is.vpn.vpn-gateway.delete   | VPN Gateway was deleted |
| vpn  | is.vpn.vpn-gateway.update   | VPN Gateway was updated |
| vpn  | is.vpn.vpn-connection.create   | VPN connection was created on VPN Gateway |
| vpn  | is.vpn.vpn-connection.delete   | VPN connection was deleted from VPN Gateway |
| vpn  | is.vpn.vpn-connection.update   | VPN connection was updated on VPN Gateway |
| vpn  | is.vpn.vpn-connection_local-cidr.create   | Local subnet was created on VPN Connection |
| vpn  | is.vpn.vpn-connection_local-cidr.delete   | Local subnet was deleted from VPN Connection |
| vpn  | is.vpn.vpn-connection_peer-cidr.create   | Peer subnet was created on VPN Connection |
| vpn  | is.vpn.vpn-connection_peer-cidr.delete   | Peer subnet was deleted from VPN Connection |
| vpn  | is.vpn.ike-policy.create   | IKE policy was created |
| vpn  | is.vpn.ike-policy.delete   | IKE policy was deleted |
| vpn  | is.vpn.ike-policy.update   | IKE policy was updated |
| vpn  | is.vpn.ipsec-policy.create   | IPsec policy was created |
| vpn  | is.vpn.ipsec-policy.delete   | IPsec policy was deleted |
| vpn  | is.vpn.ipsec-policy.update   | IPsec policy was updated |

## Supported locations
{: #at-supported-locations}

The following table lists the Activity Tracker with LogDNA location for each VPC region.

| VPC Region | Activity Tracker with LogDNA Location |
|--------------|---------------------------------------|
| us-south   | Dallas  |
| us-east | Washington |
| jp-tok   | Tokyo  |
| eu-de  | Frankfurt  |
| eu-gb  | London |
| au-syd  | Sydney |

## Where to look for events
{: #at-events-ui}

When you provision an {{site.data.keyword.at_full}} instance, events are forwarded automatically to the Activity Tracker with a LogDNA service instance in its [supported location](#at-supported-locations).
