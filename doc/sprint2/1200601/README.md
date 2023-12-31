RCOMP 2021-2022 Project - Sprint 2 - Member 1200601 folder
===========================================

## ***Edifício 3***

#### Durante a realização do Sprint 2 de RCOMP, foi desenvolvida, no 'Cisco Packet Tracer', uma simulação da rede anteriormente realizada no sprint 1, para cada edifício. Cada elemento teve de adaptar as suas VLANs, as quais se encontram definidas no planning, e os respetivos IPs (IPv4 Networks) com uma simulação funcional.

###

## *Simulação total do edifício*

![B3_Total](Total.png)

### *Floor 0*

![B3_GF](Floor0.PNG)

### *Floor 1*

![B3_FF](Floor1.PNG)


### *Notas:*

* Uma vez que não era necessário neste sprint, não foi configurado **DNS** utilizando um servidor próprio para tal.

* Os **VoIP phones** não foram configurados. Apenas se desligou as VLANs nas portas entre **switch** e **VoIP phone**.

* Para uma melhor compreensão, foi anotado, debaixo dos end nodes, os seus respetivos endereços, exceto nos portáteis e telemóveis, visto que estes têm o **DHCP** ativado. Estão, também, descritas as informações relativas aos **switches**.

* Todos os configs relacionados ao **router** e os vários **switches** encontram-se na pasta "config", por uma questão de melhor organização dos ficheiros.

* A **árvore dos endereços** e a sua respetiva legenda encontram-se, em formato **jpg**, na pasta de cada elemento do grupo.

* A **simulação de rede do campus** encontra-se na pasta do sprint master (1200902) e do elemento que está encarregue do edifício 1 (1200920).


## **Informação sobre o edíficio:**

- Backbone: 120 nodes
- End user outlets on the ground floor: 35 nodes
- End user outlets on floor one: 50 nodes
- Wi-Fi network: 55 nodes
- Local servers and administration workstations (DMZ): 28 nodes
- VoIP (IP-phones): 25 nodes
- Total nodes: 193 nodes


## Distribuição da rede

| VLAN NAME | VLAN ID | REQUESTED NODES | SUB NETWORK ADDRESS | MASK            | ADDRESS RANGE      | NETWORK ADDRESS | BROADCAST ADDRESS | FIRST VALID NODE ADDRESS | LAST VALID NODE ADDRESS |
|:----------|:--------|:----------------|:--------------------|:----------------|:-------------------|:----------------|:------------------|:-------------------------|:------------------------|
| BACKBONE  | 365     | 120             | 172.17.168.0        | 255.255.255.128 | 172.17.168.0-127   | 172.17.168.0    | 172.17.168.127    | 172.17.168.1             | 172.17.168.126          |
| GF_B3     | 376     | 35              | 172.17.172.128      | 255.255.255.192 | 172.17.172.128-163 | 172.17.172.129  | 172.17.172.128    | 172.17.172.130           | 172.17.172.162          |
| FF_B3     | 377     | 50              | 172.17.172.0        | 255.255.255.192 | 172.17.172.0-50    | 172.17.172.1    | 172.17.172.0      | 172.17.172.2             | 172.17.172.49           |
| WIFI_B3   | 378     | 55              | 172.17.171.64       | 255.255.255.192 | 172.17.171.64-119  | 172.17.171.65   | 172.17.171.64     | 172.17.171.66            | 172.17.171.118          |
| DMZ_B3    | 379     | 28              | 172.17.172.192      | 255.255.255.224 | 172.17.172.192-220 | 172.17.172.193  | 172.17.172.192    | 172.17.172.194           | 172.17.172.219          |
| VoIP_B3   | 380     | 25              | 172.17.173.32       | 255.255.255.224 | 172.17.173.32-57   | 172.17.173.33   | 172.17.173.32     | 172.17.173.34            | 172.17.173.56           |


## SubInterfaces

| VLAN NAME | VLAN ID | SUBINTERFACE      | IP ADDRESS     | MASK            |
|:----------|:--------|:------------------|:---------------|:----------------|
| GF_B3     | 376     | FastEthernet1/0.3 | 172.17.172.129 | 255.255.255.192 |
| FF_B3     | 377     | FastEthernet1/0.2 | 172.17.172.1   | 255.255.255.192 |
| WIFI_B3   | 378     | FastEthernet1/0.1 | 172.17.171.65  | 255.255.255.192 |
| DMZ_B3    | 379     | FastEthernet1/0.4 | 172.17.172.193 | 255.255.255.224 |
| VoIP_B3   | 380     | FastEthernet1/0.5 | 172.17.173.33  | 255.255.255.224 |


## Routing table

### Router B3
| Network        | Mask            | Next Hop       |
|----------------|-----------------|----------------|
| 0.0.0.0        | 0.0.0.0         | 172.17.168.1   |

###

## Explicações e observações

* O router apresenta um default route, conseguido através do endereço **0.0.0.0/0**, assim, este redireciona, quando tráfego relativo a **IPs desconhecidos**, para o **Top Router**.


* A simulação permite a comunicação entre **VLANs** (utilizando **Default Gateways**). Cada **router** encaminha qualquer endereço que não conhece para o **router** presente no MC e este encaminha para cada edifício, caso este esteja compreeendido entre os endereços do **campus**. No caso de não estar, dá forward para o **ISP** através de um **DSL Modem** (sendo esta solução representada apenas no ficheiro campus.pkt, localizado na pasta relativa ao Edifício 1).


* Todas as ligações entre switches foram alteradas para se apresentarem em **trunk mode**, o **VTP domain** foi alterado para o domínio fornecido no enunciado (**rc22djg1**) e o switch do MC foi configurado para estar em **modo server**, sendo os restantes switches configurados para estarem no **modo client**. Assim, permitimos que todos os **switches tenham todas as VLANs na sua VLAN database** configuradas para o edifício e campus (VLAN IDs no **intervalo de 365 – 395** e descritas no ficheiro planning.md).


* Na configuração deste edifício, podemos verificar tanto o IC, bem como os dois HCs e os seis CPs, estão representados por switches **"PT-Empty"**, tal como mencionado no enunciado.


* O modelo do router utilizado foi o *2811*, tal como mencionado no enunciado do projeto.


* Por outro lado, conectados aos APs, estão laptops e smartphones preparados e ligados através de WiFi à VLAN referente à WiFi Network do Edifício 4 (VLAN ID: 383).


* SSIDs e canais foram configurados nos Access Points (também representados nas imagens).

