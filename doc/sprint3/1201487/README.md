RCOMP 2021-2022 Project - Sprint 2 - Member 1200601 folder
===========================================

## ***Edifício 3***

#### Durante a realização do Sprint 3 de RCOMP, foi desenvolvida, no 'Cisco Packet Tracer', uma melhoria da rede anteriormente realizada no sprint 2, para o campus completo. Cada elemento teve de adaptar e atualizar os seus edifícios com novas informações.

### Ilustração do building 4 no Campus

![BUILDING4](Building_4.PNG)

## *DNS*

<br>

Tabela, com os glue records do DNS:

![DNS](Building_4_DNS.PNG)


<br>
<br>

Tabela de DNS, com cada record especificado:

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-4.rcomp-21-22-dj-g1         | NS       | ns.building-4.rcomp-21-22-dj-g1      |
| dns.building-4.rcomp-21-22-dj-g1     | CNAME    | ns.building-4.rcomp-21-22-dj-g1      | 
| ns.building-4.rcomp-21-22-dj-g1      | A RECORD | 172.17.173.130                       |
| server1.building-4.rcomp-21-22-dj-g1 | A RECORD | 172.17.173.131                       | 
| web.building-4.rcomp-21-22-dj-g1     | CNAME    | server1.building-4.rcomp-21-22-dj-g1 | 
| www.building-4.rcomp-21-22-dj-g1     | CNAME    | server1.building-4.rcomp-21-22-dj-g1 |


##  VoIP

### Building 3

| Ephone | Number    |
|--------|-----------|
| 1      | 966555040 |
| 2      | 966555041 | 

## OSPF

| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.172.224 | 0.0.0.31         | 4           |
| 172.17.171.128 | 0.0.0.63         | 4           | 
| 172.17.170.128 | 0.0.0.127        | 4           |
| 172.17.173.128 | 0.0.0.15         | 4           | 
| 172.17.173.112 | 0.0.0.15         | 4           | 
| 172.17.168.0   | 0.0.0.127        | 0           |

##NAT

###B4 Static NAT
* ip nat inside source static tcp 172.17.173.131 53 15.203.48.66 53
* ip nat inside source static udp 172.17.173.131 53 15.203.48.66 53
* ip nat inside source static tcp 172.17.173.130 80 15.203.48.66 803
* ip nat inside source static tcp 172.17.173.130 443 15.203.48.66 804

Como especificado no planning, o NAT para converter as redes locais para o ISP está feito no TOP_ROUTER.

