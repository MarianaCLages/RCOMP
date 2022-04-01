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

  * **The naming of the routers will follow the following structure:** Router_[BuildingNumber]
  * **The naming of the switches (ICs and HCs) will follow the following structure:** Switch_[SwitchType]\_[BuildingNumber]_[FloorNumber]
  * **The naming of the switches (CPs) will follow the following structure:** Switch_[SwitchType]\_[BuildingNumber]\_[FloorNumber]_[RoomNumber]

        [BuildingNumber] - Número identificador de cada edifício (1 a 5).
        [SwitchType] - Tipo do switch (IC, HC, CP).
        [FloorNumber] - Número identificador de cada piso (Floor zero = F0 ou Floor one = F1).
        [RoomNumber] - Número identificador de cada sala.


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

