RCOMP 2021-2022 Project - Sprint 2 planning
===========================================
### Sprint master: 1200902 ###

# 1. Sprint's backlog #
| Task  | Task Description                                                                                                                                                                                         |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| T.2.1 | Development of a layer two and layer three Packet Tracer simulation for building one, encompassing the campus backbone. Integration of every member’s Packet Tracer simulation into a single simulation. |
| T.2.2 | Development of a layer two and layer three Packet Tracer simulation for building two, encompassing the campus backbone.                                                                                  |
| T.2.3 | Development of a layer two and layer three Packet Tracer simulation for building three, encompassing the campus backbone.                                                                                |
| T.2.4 | Development of a layer two and layer three Packet Tracer simulation for building four, encompassing the campus backbone.                                                                                 |


# 2. Technical decisions and coordination #

  * **Packet Tracer version:** 8.1.1.0022
  * **Backbone cable type:** Optic fibre (multimode)
  * **VTP domain name:** rc22djg1
  * **VLAN IDs range:** 365 - 395
  * **Default VLAN ID:** 1
  * **IPv4 address space to be used:** 172.17.168.0/21
  * **ISP router IPv4 node address:** 15.203.48.66/30


  * The **naming of the servers** will follow the following structure: Server_B[BuildingNumber]
  * The **naming of the routers** will follow the following structure: Router_B[BuildingNumber]
  * The **naming of the switches (MCs e ICs)** will follow the following structure: Switch_[SwitchType]_B[BuildingNumber]
  * The **naming of the switches (HCs)** will follow the following structure: Switch_HC_B[BuildingNumber]_[Floor]
  * The **naming of the switches (CPs)** will follow the following structure: Switch_CP_B[BuildingNumber]\_[Floor]_[ID]
  * The **naming of the access points (APs)** will follow the following structure: AccessPoint_B[BuildingNumber]_[Floor]
  * The **naming of the PCs** will follow the following structure: PC_[Floor]_[ID]
  * The **naming of the laptops** will follow the following structure: Laptop_[Floor]_[ID]
  * The **naming of the phones** will follow the following structure: IP_Phone_[Floor]_[ID]
  * The **naming of the smartphones** will follow the following structure: Smartphone_[Floor]_[ID]

          [BuildingNumber] - Identifier number of each building (1 to 4)
          [SwitchType] - The switch type (MC or IC)
          [Floor] - Identifier number of each floor (GF = Ground Floor or FF = First Floor)
          [ID] - Identifier number of each device (starting from 1, ascending order)

### *Notes:*

  * In order to have functional laptops and smartphones via wireless, we decided to configure a DHCP Pool in each building.


## *VLANs and its respective networks*

| VLAN ID | VLAN Name | Network Address   |
|---------|-----------|-------------------|
| 365     | BackBone  | 172.17.168.0/25   |
| 366     | GF_B1     | 172.17.171.0/26   |
| 367     | FF_B1     | 172.17.170.0/25   |
| 368     | Wifi_B1   | 172.17.168.128/25 |
| 369     | DMZ_B1    | 172.17.169.128/25 |
| 370     | VoIP_B1   | 172.17.172.64/26  |
| 371     | GF_B2     | 172.17.173.0/27   |
| 372     | FF_B2     | 172.17.171.192/26 |
| 373     | Wifi_B2   | 172.17.169.0/25   |
| 374     | DMZ_B2    | 172.17.173.64/28  |
| 375     | VoIP_B2   | 172.17.173.96/28  |
| 376     | GF_B3     | 172.17.172.128/26 |
| 377     | FF_B3     | 172.17.172.0/26   |
| 378     | Wifi_B3   | 172.17.171.64/26  |
| 379     | DMZ_B3    | 172.17.172.192/27 |
| 380     | VoIP_B3   | 172.17.173.32/27  |
| 381     | GF_B4     | 172.17.172.224/27 |
| 382     | FF_B4     | 172.17.171.128/26 |
| 383     | Wifi_B4   | 172.17.170.128/25 |
| 384     | DMZ_B4    | 172.17.173.128/28 |
| 385     | VoIP_B4   | 172.17.173.112/28 |
| 386     |           |                   |
| 387     |           |                   |
| 388     |           |                   |
| 389     |           |                   |
| 390     |           |                   |
| 391     |           |                   |
| 392     |           |                   |
| 393     |           |                   |
| 394     |           |                   |
| 395     |           |                   |

### *Notes:*

* Since our group only has 4 elements, there is no need to configure all the other available VLANs.


## *Buildings and respective backbone IPv4 Addresses*

| Building | IPv4 Network |
|----------|--------------|
| 1        | 172.17.168.5 |
| 2        | 172.17.168.2 |
| 3        | 172.17.168.3 |
| 4        | 172.17.168.4 |


# 3. Subtasks assignment #

  * **1200601** - Development of a layer two and layer three Packet Tracer simulation for **building three**, encompassing the campus backbone.
  * **1200902** - Development of a layer two and layer three Packet Tracer simulation for **building two**, encompassing the campus backbone.
  * **1200920** - Development of a layer two and layer three Packet Tracer simulation for **building one**, encompassing the campus backbone. Integration of every member’s Packet Tracer simulation into a single simulation.
  * **1201487** - Development of a layer two and layer three Packet Tracer simulation for **building four**, encompassing the campus backbone.

