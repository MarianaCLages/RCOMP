RCOMP 2021-2022 Project - Sprint 2 - Member 1200902 folder
===========================================

## ***Edifício 2***

#### Durante a realização do Sprint 2 de RCOMP, foi desenvolvida, no 'Cisco Packet Tracer', uma simulação da rede anteriormente realizada no sprint 1, para cada edifício. Cada elemento teve de adaptar as suas VLANs, as quais se encontram definidas no planning, e os respetivos IPs (IPv4 Networks) com uma simulação funcional.

###

### *Simulação total do edifício*

![B2_Total](Building2_Total.png)


### *Piso 0*

![B2_GF](Building2_GroundFloor.png)


### *Piso 1*

![B2_FF](Building2_FirstFloor.png)


### *Notas:*

* Uma vez que não era necessário neste sprint, não foi configurado **DNS** utilizando um servidor próprio para tal.

* Foi configurada uma DHCP Pool no router, chamada **"Wifi_B2"**, que está encarregue de atribuir enderenços **IPv4** a todos os dipositivos que se liguem de forma wireless à rede.

* Os **VoIP phones** não foram configurados. Apenas se desligou as VLANs nas portas entre **switch** e **VoIP phone**.

* Para uma melhor compreensão, foi anotado, debaixo dos end nodes, os seus respetivos endereços, exceto nos portáteis e telemóveis, visto que estes têm o **DHCP** ativado. Estão, também, descritas as informações relativas aos **switches**.

* Todos os configs relacionados ao **router** e os vários **switches** encontram-se na pasta "config", por uma questão de melhor organização dos ficheiros.


### *Informação sobre o edifício:*

- End user outlets on the ground floor: 25 nodes
- End user outlets on floor one: 50 nodes
- Wi-Fi network: 120 nodes
- DMZ (Servers, administration workstations, and network infrastructure devices): 12 nodes
- VoIP (IP-phones): 12 nodes


## Distribuição da rede

| VLAN NAME | VLAN ID | REQUESTED NODES | SUB NETWORK ADDRESS | MASK            | ADDRESS RANGE      | NETWORK ADDRESS | BROADCAST ADDRESS | FIRST VALID NODE ADDRESS | LAST VALID NODE ADDRESS |
|-----------|---------|-----------------|---------------------|-----------------|--------------------|-----------------|-------------------|--------------------------|-------------------------|
| BACKBONE  | 365     | 120             | 172.17.168.0        | 255.255.255.128 | 172.17.168.0-127   | 172.17.168.0    | 172.17.168.127    | 172.17.168.1             | 172.17.168.126          |
| GF_B2     | 371     | 25              | 172.17.173.0        | 255.255.255.224 | 172.17.173.0-31    | 172.17.173.0    | 172.17.173.31     | 172.17.173.1             | 172.17.173.30           |
| FF_B2     | 372     | 50              | 172.17.171.192      | 255.255.255.192 | 172.17.171.192-255 | 172.17.171.192  | 172.17.171.255    | 172.17.171.193           | 172.17.171.254          |
| Wifi_B2   | 373     | 120             | 172.17.169.0        | 255.255.255.128 | 172.17.169.0-127   | 172.17.169.0    | 172.17.169.127    | 172.17.169.1             | 172.17.169.126          |
| DMZ_B2    | 374     | 12              | 172.17.173.64       | 255.255.255.240 | 172.17.173.64-79   | 172.17.173.64   | 172.17.173.79     | 172.17.173.65            | 172.17.173.78           |
| VoIP_B2   | 375     | 12              | 172.17.173.96       | 255.255.255.240 | 172.17.173.96-111  | 172.17.173.96   | 172.17.173.111    | 172.17.173.97            | 172.17.173.110          |


## Routing table

| Network   | 	Mask   | Next hop     |
|-----------|---------|--------------|
| 0.0.0.0/0 | 0.0.0.0 | 172.17.168.1 |


## Explicações e observações

* O router apresenta um default route, conseguido através do endereço **0.0.0.0/0**, assim, este redireciona, quando tráfego relativo a **IPs desconhecidos**, para o **router do ISP**.

* A simulação permite a comunicação entre **VLANs** (utilizando **Default Gateways**). Cada **router** encaminha qualquer endereço que não conhece para o **router** presente no MC e este encaminha para cada edifício, caso este esteja compreeendido entre os endereços do **campus**. No caso de não estar, dá forward para o **ISP** através de um **DSL Modem** (sendo esta solução representada apenas no ficheiro campus.pkt, localizado na pasta relativa ao Edifício 1).

* Todas as ligações entre switches foram alteradas para se apresentarem em **trunk mode**, o **VTP domain** foi alterado para o domínio fornecido no enunciado (**rc22djg1**) e o switch do MC foi configurado para estar em **modo server**, sendo os restantes switches configurados para estarem no **modo client**. Assim, permitimos que todos os **switches tenham todas as VLANs na sua VLAN database** configuradas para o edifício e campus (VLAN IDs no **intervalo de 365 – 395** e descritas no ficheiro planning.md).

* Na configuração deste edifício, podemos verificar tanto o IC, bem como os dois HCs e os quatro CPs, estão representados por switches **"PT-Empty"**, tal como mencionado no enunciado.

* O modelo do router utilizado foi o *2811*, tal como mencionado no enunciado do projeto.

* Por outro lado, conectados aos APs, estão laptops e smartphones preparados e ligados através de WiFi à VLAN referente à WiFi Network do Edifício 4 (VLAN ID: 383).

* SSIDs e canais foram configurados nos Access Points (também representados nas imagens).

* Tal como mencionado previamente, o DHCP foi configurado numa Pool "WIFI_B2" permitindo, assim, a atribuição automática de enderenços IPv4 a todos os end nodes que tenham o DCHP ligado.