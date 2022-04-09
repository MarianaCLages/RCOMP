## RCOMP 2021-2022 Project - Sprint 2 - Member 1200601 folder

# Building 3

## Information

- End user outlets on the ground floor: 35 nodes
- End user outlets on floor one: 50 nodes
- Wi-Fi network: 55 nodes
- Local servers and administration workstations (DMZ): 28 nodes
- VoIP (IP-phones): 25 nodes
- Total Nodes: 193 nodes

## Address Distribuction

| VLAN NAME | VLAN ID | REQUESTED NODES | SUB NETWORK ADDRESS | MASK            | ADDRESS RANGE      | NETWORK ADDRESS | BROADCAST ADDRESS | FIRST VALID NODE ADDRESS | LAST VALID NODE ADDRESS |
|:----------|:--------|:----------------|:--------------------|:----------------|:-------------------|:----------------|:------------------|:-------------------------|:------------------------|
| GF_B3     | 376     | 35              | 172.17.171.128      | 255.255.255.192 | 172.17.171.128-163 | 172.17.171.129  | 172.17.171.128    | 172.17.171.130           | 172.17.171.162          |
| FF_B3     | 377     | 50              | 172.17.172.0        | 255.255.255.192 | 172.17.172.0-50    | 172.17.172.1    | 172.17.172.0      | 172.17.172.2             | 172.17.172.49           |
| WIFI_B3   | 378     | 55              | 172.17.171.64       | 255.255.255.192 | 172.17.171.64-119  | 172.17.171.65   | 172.17.171.64     | 172.17.171.66            | 172.17.171.118          |
| DMZ_B3    | 379     | 28              | 172.17.169.192      | 255.255.255.224 | 172.17.169.192-220 | 172.17.169.193  | 172.17.169.192    | 172.17.169.194           | 172.17.169.219          |
| VoIP_B3   | 380     | 25              | 172.17.173.32       | 255.255.255.224 | 172.17.173.32-57   | 172.17.173.33   | 172.17.173.32     | 172.17.173.34            | 172.17.173.56           |

##Router VLAN

| VLAN NAME | VLAN NAME | IP ADDRESS     | MASK            |
|:----------|:----------|:---------------|:----------------|
| DMZ_B3    | 379       |  172.17.172.129 | 255.255.255.224 |

##SubInterfaces

| VLAN NAME | VLAN ID | SUBINTERFACE                               | IP ADDRESS     | MASK            |
|:----------|:--------|:-------------------------------------------|:---------------|:----------------|
| GF_B3     | 376     | FastEthernet1/0.3                          | 172.17.172.129 | 255.255.255.192 |
| FF_B3     | 377     | FastEthernet1/0.2                          | 172.17.172.1   | 255.255.255.192 |
| WIFI_B3   | 378     | FastEthernet1/0.1                          | 172.17.171.65  | 255.255.255.192 |
| VoIP_B3   | 380     | FastEthernet1/0.5                          | 172.17.173.33  | 255.255.255.224 |

#Switch
