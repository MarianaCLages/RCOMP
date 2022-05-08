RCOMP 2021-2022 Project - Sprint 2 - Member 1200601 folder
===========================================

## ***Edifício 3***

#### Durante a realização do Sprint 1 de RCOMP, foi desenvolvida, no 'Cisco Packet Tracer', uma melhoria da rede anteriormente realizada no sprint 2, para o campus completo. Cada elemento teve de adaptar e atualizar os seus edifícios com novas informações.

### Ilustração do building 4 no Campus

![BUILDING4](Building_2.PNG)

## *DNS*

<br>

Tabela, com os glue records do DNS:

![DNS](Building_2_DNS.PNG)


<br>
<br>

Tabela de DNS, com cada record especificado:

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-2.rcomp-21-22-dj-g1         | NS       | ns.building-2.rcomp-21-22-dj-g1      |
| dns.building-2.rcomp-21-22-dj-g1     | CNAME    | ns.building-2.rcomp-21-22-dj-g1      | 
| ns.building-2.rcomp-21-22-dj-g1      | A RECORD | 172.17.173.65                        |
| server1.building-2.rcomp-21-22-dj-g1 | A RECORD | 172.17.173.66                        | 
| web.building-2.rcomp-21-22-dj-g1     | CNAME    | server1.building-2.rcomp-21-22-dj-g1 | 
| www.building-2.rcomp-21-22-dj-g1     | CNAME    | server1.building-2.rcomp-21-22-dj-g1 |



##  VoIP

### Building 2

| Ephone | Number    |
|--------|-----------|
| 1      | 966555020 |
| 2      | 966555021 | 

## OSPF
| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.168.0   | 0.0.0.127        | 0           |
| 172.17.173.0   | 0.0.0.31         | 2           | 
| 172.17.171.192 | 0 0.0.63         | 2           |
| 172.17.169.0   | 0.0.0.127        | 2           | 
| 172.17.173.96  | 0.0.0.15         | 2           | 
| 172.17.173.64  | 0.0.0.14         | 2           |

##NAT

###B2 Static NAT
* ip nat inside source static tcp 172.17.173.66 53 15.203.48.66 53
* ip nat inside source static udp 172.17.173.66 53 15.203.48.66 53
* ip nat inside source static tcp 172.17.173.65 80 15.203.48.66 807
* ip nat inside source static tcp 172.17.173.65 443 15.203.48.66 808

Como especificado no planning, o NAT para converter as redes locais para o ISP está feito no TOP_ROUTER.

