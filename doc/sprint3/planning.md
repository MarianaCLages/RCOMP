RCOMP 2021-2022 Project - Sprint 3 planning
===========================================

### Sprint master: 1200601

(This file is to be created/edited by the sprint master only)


# 1. Sprint's backlog #

| Task  | Task Description                                                                                                                                                                                                                                           |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T.3.1 | Update the building1.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 1                                                                                                    |
| T.3.2 | Update the building2.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 2. Final integration of each member's Packet Tracer simulation into a single simulation (campus.pkt) |
| T.3.3 | Update the building3.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 3                                                                                                    |
| T.3.4 | Update the building4.pkt layer three Packet Tracer simulation from the previous sprint, to include the described features in this sprint for building 4                                                                                                    |


# 2. Technical decisions and coordination #

In this section, all technical decisions taken in the planning meeting should be mentioned. Most importantly, all
technical decisions impacting on the subtasks implementation must be settled on this meeting and specified here.

In this sprint, the team needs to work on the tasks only using the campus.pkt file. However, each team member must also
commit to the **personal sprint folder a text file with a configuration dump for every switch and for every router
within the encompassed building. These configuration text files can be easily exported in Packet Tracer: within the
device’s window click the export button on the Running Config, or the Startup Config (if the Running Config has been
saved).**


## 3. OSPF

### Building 1

| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.171.0   | 0.0.0.63         | 1           |
| 172.17.170.0   | 0.0.0.127        | 1           | 
| 172.17.168.128 | 0.0.0.127        | 1           |
| 172.17.169.128 | 0.0.0.127        | 1           | 
| 172.17.172.64  | 0.0.0.63         | 1           | 
| 172.17.168.0   | 0.0.0.127        | 0           |

One DNS domain is going to be established on each building.

### Building 2

| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.168.0   | 0.0.0.127        | 0           |
| 172.17.173.0   | 0.0.0.31         | 2           | 
| 172.17.171.192 | 0 0.0.63         | 2           |
| 172.17.169.0   | 0.0.0.127        | 2           | 
| 172.17.173.96  | 0.0.0.15         | 2           | 
| 172.17.173.64  | 0.0.0.14         | 2           |


### Building 3

| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.168.0   | 0.0.0.127        | 0           |
| 172.17.172.128 | 0.0.0.63         | 3           | 
| 172.17.172.0   | 0 0.0.63         | 3           |
| 172.17.171.64  | 0.0.0.63         | 3           | 
| 172.17.172.192 | 0.0.0.31         | 3           | 
| 172.17.173.32  | 0.0.0.31         | 3           |


### Building 4

| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.172.224 | 0.0.0.31         | 4           |
| 172.17.171.128 | 0.0.0.63         | 4           | 
| 172.17.170.128 | 0.0.0.127        | 4           |
| 172.17.173.128 | 0.0.0.15         | 4           | 
| 172.17.173.112 | 0.0.0.15         | 4           | 
| 172.17.168.0   | 0.0.0.127        | 0           |

## 4. VoIP

### Building 1

| Ephone | Number    |
|--------|-----------|
| 1      | 966555010 |
| 2      | 966555011 | 
| 3      | 966555012 |
| 4      | 966555013 | 

### Building 2

| Ephone | Number    |
|--------|-----------|
| 1      | 966555020 |
| 2      | 966555021 | 


### Building 3

| Ephone | Number    |
|--------|-----------|
| 1      | 966555030 |
| 2      | 966555031 | 


### Building 4

| Ephone | Number    |
|--------|-----------|
| 1      | 966555040 |
| 2      | 966555041 | 


## 5. DNS Database

## DNS Domain

One DNS domain is going to be established on each building.

The team member in charge of building 1 will create a DNS domain name matching the team’s repository name (
rcomp-21-22-cc-gn). This is going to be the highest-level domain, so it’s going to be used as if it was the DNS root
domain.

DNS name for the remaining members: **building-X.rcomp-21-22-cc-gn**

With **X** replaced by the digit that identifies the building (i.e., 2, 3, 4, and 5).

### *Notes:*

Since we are a team of four members a DNS for the fifth building won't be developed.

### Building 1

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-1.rcomp-21-22-dj-g1         | NS       | ns.building-1.rcomp-21-22-dj-g1      |
| dns.building-1.rcomp-21-22-dj-g1     | CNAME    | ns.building-1.rcomp-21-22-dj-g1      | 
| ns.building-1.rcomp-21-22-dj-g1      | A RECORD | 172.17.169.140                       |
| server1.building-1.rcomp-21-22-dj-g1 | A RECORD | 172.17.169.130                       | 
| web.building-1.rcomp-21-22-dj-g1     | CNAME    | server1.building-1.rcomp-21-22-dj-g1 | 
| www.building-1.rcomp-21-22-dj-g1     | CNAME    | server1.building-1.rcomp-21-22-dj-g1 |


### Building 2

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-2.rcomp-21-22-dj-g1         | NS       | ns.building-2.rcomp-21-22-dj-g1      |
| dns.building-2.rcomp-21-22-dj-g1     | CNAME    | ns.building-2.rcomp-21-22-dj-g1      | 
| ns.building-2.rcomp-21-22-dj-g1      | A RECORD | 172.17.173.65                        |
| server1.building-2.rcomp-21-22-dj-g1 | A RECORD | 172.17.173.66                        | 
| web.building-2.rcomp-21-22-dj-g1     | CNAME    | server1.building-2.rcomp-21-22-dj-g1 | 
| www.building-2.rcomp-21-22-dj-g1     | CNAME    | server1.building-2.rcomp-21-22-dj-g1 |


### Building 3

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-3.rcomp-21-22-dj-g1         | NS       | ns.building-3.rcomp-21-22-dj-g1      |
| dns.building-3.rcomp-21-22-dj-g1     | CNAME    | ns.building-3.rcomp-21-22-dj-g1      | 
| ns.building-3.rcomp-21-22-dj-g1      | A RECORD | 172.17.172.131                       |
| server1.building-3.rcomp-21-22-dj-g1 | A RECORD | 172.17.172.132                       | 
| web.building-3.rcomp-21-22-dj-g1     | CNAME    | server1.building-3.rcomp-21-22-dj-g1 | 
| www.building-3.rcomp-21-22-dj-g1     | CNAME    | server1.building-3.rcomp-21-22-dj-g1 |


### Building 4

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-4.rcomp-21-22-dj-g1         | NS       | ns.building-4.rcomp-21-22-dj-g1      |
| dns.building-4.rcomp-21-22-dj-g1     | CNAME    | ns.building-4.rcomp-21-22-dj-g1      | 
| ns.building-4.rcomp-21-22-dj-g1      | A RECORD | 172.17.173.130                       |
| server1.building-4.rcomp-21-22-dj-g1 | A RECORD | 172.17.173.131                       | 
| web.building-4.rcomp-21-22-dj-g1     | CNAME    | server1.building-4.rcomp-21-22-dj-g1 | 
| www.building-4.rcomp-21-22-dj-g1     | CNAME    | server1.building-4.rcomp-21-22-dj-g1 |


## 6. NAT

In this sprint, NAT will be used as static for each server of each building, and will be used aswell in the TOP_ROUTER to make the connection between the ISP and the local network.

##Static NAT
###B1 Static NAT
* ip nat inside source static tcp 172.17.177.130 53 15.203.48.69 53
* ip nat inside source static udp 172.17.177.130 53 15.203.48.69 53
* ip nat inside source static tcp 172.17.177.140 80 15.203.48.69 800
* ip nat inside source static tcp 172.17.177.140 443 15.203.48.69 801

###B2 Static NAT
* ip nat inside source static tcp 172.17.173.66 53 15.203.48.66 53
* ip nat inside source static udp 172.17.173.66 53 15.203.48.66 53
* ip nat inside source static tcp 172.17.173.65 80 15.203.48.66 807
* ip nat inside source static tcp 172.17.173.65 443 15.203.48.66 808


###B3 Static NAT
* ip nat inside source static tcp 172.17.172.132 53 15.203.48.66 53
* ip nat inside source static udp 172.17.172.132 53 15.203.48.66 53
* ip nat inside source static tcp 172.17.172.131 80 15.203.48.66 805
* ip nat inside source static tcp 172.17.172.131 443 15.203.48.66 806

###B4 Static NAT
* ip nat inside source static tcp 172.17.173.131 53 15.203.48.66 53
* ip nat inside source static udp 172.17.173.131 53 15.203.48.66 53
* ip nat inside source static tcp 172.17.173.130 80 15.203.48.66 803
* ip nat inside source static tcp 172.17.173.130 443 15.203.48.66 804

## 7. Access Lists
### Anti-Spoofing

In this specific scenario, we are going to apply Access Lists in order to prevent DOS or DDOS. In order to make this happen, we will have to define access lists with all the local networks in the system both permit and deny.
Since it's a good practice to use the ACLs sooner in the network as possible, we are going to use the same in the TOP_ROUTER, where it connects the outside connection (ISP) with the local network using the NAT protocol.

# 8. Subtasks assignment #

* **1200601** - Update the building3.pkt layer three Packet Tracer simulation from the previous sprint, to include the
  described features in this sprint for **building three**.
* **1200902** - Update the building2.pkt layer three Packet Tracer simulation from the previus sprint, to include the
  described features in this sprint for **building two**. Final integration of each member's Packet Tracer simulation
  into a single simulation (campus.pkt).
* **1200920** - Update the building1.pkt layer three Packet Tracer simulation from the previous sprint, to include the
  described features in this sprint for **building one**.
* **1201487** - Update the building4.pkt layer three Packet Tracer simulation from the previous sprint, to include the
  described features in this sprint for **building four**.
