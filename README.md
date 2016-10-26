cloudcoreo-vpc
==============

This [CloudCoreo](http://www.cloudcoreo.com) repository will set up a VPC from scratch with public and private subnets across 3 AZ's. In addition, it will create and maintain a <b>mostly-available</b> NAT instance in the public subnets.

* <b>Mostly-Available</b> refers to the fact that the HA will go down in the event of its AZ outage, but auto scaling will relaunch in a different AZ ensuring minimum downtime of the NAT

## description
A VPC in 3 datacenters with public and private subnets and an HA-NAT

## tags
1. Network
1. VPC
1. NAT
1. High Availability

## Categories

1. Network

<h3>OVERRIDE REQUIRED VARIABLES</h3>
* <b>NONE</b>

<h3>OVERRIDE OPTIONAL VARIABLES</h3>
* <b>VPC_NAME:</b>
  * required: true
  * description: this is the name of your vpc as defined by your [CloudCoreo](http://www.cloudcoreo.com) setup
  * default: my-vpc
* <b>NAT_NAME:</b>
  * required: true
  * description: this is the name of your NAT as defined by your [CloudCoreo](http://www.cloudcoreo.com) setup
  * default: NAT
* <b>VPC_OCTETS:</b>
  * required: true
  * description: the octets for the vpc ip range - i.e. xxx.xxx.xxx.xxx
  * default: 10.0.0.0
* <b>PUBLIC_SUBNET_NAME:</b>
  * required: true
  * description: the [CloudCoreo](http://www.cloudcoreo.com) name of the public vpc subnets
  * default: my-public-subnet
* <b>PUBLIC_ROUTE_NAME:</b>
  * required: true
  * description: the name to give to the public route
  * default: my-public-route
* <b>PRIVATE_SUBNET_NAME:</b>
  * required: true
  * description: the [CloudCoreo](http://www.cloudcoreo.com) name of the private vpc subnets
  * default: my-private-subnet
* <b>PRIVATE_ROUTE_NAME:</b>
  * required: true
  * description: the name to give to the private route
  * default: my-private-route
