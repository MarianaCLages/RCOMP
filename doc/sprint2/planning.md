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
  * **Backbone cable type:** Optic fibre
  * **VTP domain name:** rc22djg1
  * **VLAN IDs range:** 365 - 395
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


| Building     | IPv4 Networks |
|--------------|---------------|
| 1 + Backbone |               |
| 2            |               |
| 3            |               |
| 4            |               |


| VLAN ID | VLAN Name |
|---------|-----------|
| 365     | backbone  |
| 366     | GF_B1     |
| 367     | FF_B1     |
| 368     | Wifi_B1   |
| 369     | DMZ_B1    |
| 370     | VoIP_B1   |
| 371     | GF_B2     |
| 372     | FF_B2     |
| 373     | Wifi_B2   |
| 374     | DMZ_B2    |
| 375     | VoIP_B2   |
| 376     | GF_B3     |
| 377     | FF_B3     |
| 378     | Wifi_B3   |
| 379     | DMZ_B3    |
| 380     | VoIP_B3   |
| 381     | GF_B4     |
| 382     | FF_B4     |
| 383     | Wifi_B4   |
| 384     | DMZ_B4    |
| 385     | VoIP_B4   |
| 386     |           |
| 387     |           |
| 388     |           |
| 389     |           |
| 390     |           |
| 391     |           |
| 392     |           |
| 393     |           |
| 394     |           |
| 395     |           |


# 3. Subtasks assignment #

  * 1200601 - Development of a layer two and layer three Packet Tracer simulation for building three, encompassing the campus backbone.
  * 1200902 - Development of a layer two and layer three Packet Tracer simulation for building two, encompassing the campus backbone.
  * 1200920 - Development of a layer two and layer three Packet Tracer simulation for building one, encompassing the campus backbone. Integration of every member’s Packet Tracer simulation into a single simulation.
  * 1201487 - Development of a layer two and layer three Packet Tracer simulation for building four, encompassing the campus backbone.

