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

  * **The naming of the servers will follow the following structure:** Server_B[BuildingNumber]
  * **The naming of the routers will follow the following structure:** Router_B[BuildingNumber]
  * **The naming of the switches (MCs) will follow the following structure:** Switch_MC_B[BuildingNumber]
  * **The naming of the switches (ICs and HCs) will follow the following structure:** Switch_[SwitchType]\_B[BuildingNumber]_F[FloorNumber]
  * **The naming of the switches (CPs) will follow the following structure:** Switch_CP_B[BuildingNumber]\_F[FloorNumber]_[SwitchNumber]

        [BuildingNumber] - Identifier number of each building (1 to 5)
        [SwitchType] - The switch type (IC or HC)
        [FloorNumber] - Identifier number of each floor (floor zero = 0 or floor one = 1)
        [SwitchNumber] - Identifier number of each switch (starting from 1, ascending order)


| Building     | IPv4 Networks |
|--------------|---------------|
| 1 + Backbone |               |
| 2            |               |
| 3            |               |
| 4            |               |
| 5            |               |


| VLAN ID | VLAN Name |
|---------|-----------|
| 365     |           |
| 366     |           |
| 367     |           |
| 368     |           |
| 369     |           |
| 370     |           |
| 371     |           |
| 372     |           |
| 373     |           |
| 374     |           |
| 375     |           |
| 376     |           |
| 377     |           |
| 378     |           |
| 379     |           |
| 380     |           |
| 381     |           |
| 382     |           |
| 383     |           |
| 384     |           |
| 385     |           |
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

