RCOMP 2021-2022 Project - Sprint 2 - Member 1200601 folder
===========================================

## ***Edifício 3***

#### Durante a realização do Sprint 1 de RCOMP, foi desenvolvida, no 'Cisco Packet Tracer', uma melhoria da rede anteriormente realizada no sprint 2, para o campus completo. Cada elemento teve de adaptar e atualizar os seus edifícios com novas informações.

### Ilustração do building 4 no Campus

![BUILDING4](Building_1.PNG)

## *DNS*

<br>

Tabela, com os glue records do DNS:

![DNS](Building_1_DNS.PNG)


<br>
<br>

Tabela de DNS, com cada record especificado:

| Name                                 | Type     | Detail                               |
|--------------------------------------|----------|--------------------------------------|
| building-1.rcomp-21-22-dj-g1         | NS       | ns.building-1.rcomp-21-22-dj-g1      |
| dns.building-1.rcomp-21-22-dj-g1     | CNAME    | ns.building-1.rcomp-21-22-dj-g1      | 
| ns.building-1.rcomp-21-22-dj-g1      | A RECORD | 172.17.169.140                       |
| server1.building-1.rcomp-21-22-dj-g1 | A RECORD | 172.17.169.130                       | 
| web.building-1.rcomp-21-22-dj-g1     | CNAME    | server1.building-1.rcomp-21-22-dj-g1 | 
| www.building-1.rcomp-21-22-dj-g1     | CNAME    | server1.building-1.rcomp-21-22-dj-g1 |


##  VoIP

### Building 1

| Ephone | Number    |
|--------|-----------|
| 1      | 966555010 |
| 2      | 966555011 | 
| 3      | 966555012 |
| 4      | 966555013 | 

## OSPF
| Network-Adress | Network-Wildcard | Area Number |
|----------------|------------------|-------------|
| 172.17.171.0   | 0.0.0.63         | 1           |
| 172.17.170.0   | 0.0.0.127        | 1           | 
| 172.17.168.128 | 0.0.0.127        | 1           |
| 172.17.169.128 | 0.0.0.127        | 1           | 
| 172.17.172.64  | 0.0.0.63         | 1           | 
| 172.17.168.0   | 0.0.0.127        | 0           |

##NAT

###B1 Static NAT
* ip nat inside source static tcp 172.17.177.130 53 15.203.48.69 53
* ip nat inside source static udp 172.17.177.130 53 15.203.48.69 53
* ip nat inside source static tcp 172.17.177.140 80 15.203.48.69 800
* ip nat inside source static tcp 172.17.177.140 443 15.203.48.69 801

Como especificado no planning, o NAT para converter as redes locais para o ISP está feito no TOP_ROUTER.

