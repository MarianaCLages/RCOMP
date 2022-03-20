# RCOMP 2021-2022 Project - Sprint 1 - Member 1200601 folder


# Introdução

Este projeto tem como objetivo criar uma estrutura de cabeamento em cinco
edifícios, cada edifícios está associado a um número. A equipa decidiu que cada membro ficaria
com um edifício para planear o cabeamento do mesmo, no meu caso, fiquei com o edifício 3.

A imagem abaixo mostra o posicionamento dos edifícios, sendo o edifício 1 o data center.
Também se é mostrado os cabos situados a baixo da terra para mostrar a conexão entre todos os edifícios:


![AllBuildings](AllBuildings.PNG)




# Edifício 3

O edifício 3 tem uma área de 400 metros quadrados e tem dois pisos, sendo que o rés do chão tem 11 salas sendo que
duas delas são casas de banhos, os professores envolvidos neste projeto informaram-nos
que não seria necessário relacionar qualquer tipo de cabeamento nestas duas salas. 
O piso 1 tem 12 salas sendo que duas também são casas de banho, a mesma regra indicada anteriormente
também se aplica aqui.


# Cabeamento do Rés-do-chão

Começemos por apresentar a planta do rés do chão e o seu respetivo cabeamento:

**Planta Rés-do-chão**

![GroundFloor](FloorGroundMeasure.PNG)

**Cabeamento do Rés-do-chão (ver svg para uma melhor inspeção)**

![Floor0All](GroundFloorAll.PNG)

**Legenda:**

![Legenda](legenda.PNG)

**Informações de cada sala:**

| Sala               | Área      | Outlets   | CP                                    |
|:-------------------|:----------|:----------|:--------------------------------------|
| 3.0.1              | 15.6 m^2  | 4 Outlets | 0                                     |
| 3.0.2              | 15.6 m^2  | 4 Outlets | 0                                     |
| 3.0.3              | 15.6 m^2  | 4 Outlets | 0                                     |
| 3.0.4 (datacentre) | 18.44 m^2 | 4 Outlets | 1 (Switch e patch panel de 24 portas) |
| 3.0.5              | 29.04 m^2 | 6 Outlets | 1 (Switch e patch panel de 12 portas  |
| 3.0.6              | 29.04 m^2 | 6 Outlets | 1 (Switch e patch panel de 12 portas) |
| 3.0.7              | 29.04 m^2 | 6 Outlets | 1 (Switch e patch panel de 12 portas) |
| 3.0.8              | 14 m^2    | 4 Outlets | 1 (Switch e patch panel de 12 portas) |
| 3.0.9              | 7.82 m^2  | 0 Outlets | 0                                     |



**Tabela de Materiais:**

![TabelaDeMateriaisPiso0](TabelaDeMateriaisP0.PNG)

#Justificação dos materiais usados e do posicionamento dos mesmos

* Como temos 38 **Outlets**, 2 **APs**, 5 CPs,1 **IC** e 1 **HC**  neste piso, 
vamos precisar, no mínimo, de 38 cabos de cobre (CAT6). 

* O cabo **CAT7** que estava antes no piso 0 subiu para o piso 1 através da passagem que há
na sala 3.1.10.

* Devido á natureza da sala 3.0.4, esta foi selecionada para ser o data center
deste piso, foi colocado o **HC**, o **IC** e um **CP** que faz conexão com as salas 3.0.1 até 3.0.4.


* As salas 3.0.5,3.0.6,3.0.7 e a 3.0.8 têm os seus prórpios **CPs** cada
uma com 12 portas.


* O cabo **CAT7** é utilizado para conectar os **CPs**,**HC** e o **AP** entre eles, permitindo
assim um alto nível de tráfego de dados.Para alimentação dos AP o cabo CAT7 irá utilizar a tecnologia POE para alimentar de energia elétrica os equipamentos. Irão ser utilizados Power Injectors para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do HC para assim alimentar a ligação.


* Devido às paredes de betão armado que existem no piso, temos em consideração
que o raio do **AP** desce 10 metros que o normal.


* Para a alimentação dos **APs**, o cabo **CAT7** irá utilizar a tecnologia **PoE** (Power over Ethernet). Irão ser utilizados Power Injectors para permitir ao cabo o transporte de energia elétrica. Estes dispositivos irão ser colocados na saída do HC, para alimentar a ligação.


* Os cabos **CAT6** e **CAT7** percorrem a maior parte do edifício através das
calhas subterrâneas que foram previemente estabelecidas no edifício. 


* Na maioria das salas vão existir cabos a percorrer calhas subterrâneas já implementadas no edifício.


* Devido às paredes de betão armado que existem no piso, 
temos de ter em consideração o fator que o raio de 
alcance de cada **AP** é reduzido por volta de 10 metros, 
o que vai fazer com que seja necessário 2 **APs** no mesmo piso para que fique completamente coberto por wireless


* Decidiu-se seguir a regra em que deve-se deixar pelo menos 1/3 ou
  metade das portas dos **CPs** livres.

#Cabeamento do Piso 1
    
**Planta do Piso 1:**

![Floor1](FloorOneMeasure.PNG)

**Cabeamento do Piso 1 (ver svg para uma melhor inspeção)**

![Floor1All](FloorOneAll.PNG)

**Legenda:**

![Legenda](legenda.PNG)

| Sala   | Área      | Outlets   | CP                                    |
|:-------|:----------|:----------|:--------------------------------------|
| 3.1.1  | 24 m^2    | 6 Outlets | 0                                     |
| 3.1.2  | 24 m^2    | 6 Outlets | 1 (Switch e patch panel de 24 portas) |
| 3.1.3  | 21.6 m^2  | 6 Outlets | 1 (Switch e patch panel de 24 portas) |
| 3.1.4  | 32.8 m^2  | 8 Outlets | 0                                     |
| 3.1.5  | 32.8 m^2  | 8 Outlets | 1 (Switch e patch panel de 12 portas  |
| 3.1.6  | 21.6 m^2  | 6 Outlets | 0                                     |
| 3.1.7  | 42.7 m^2  | 8 Outlets | 1 (Switch e patch panel de 24 portas) |
| 3.1.8  | 42.7 m^2  | 8 Outlets | 0                                     |
| 3.1.9  | 42.7 m^2  | 8 Outlets | 1 (Switch e patch panel de 12 portas)                                     |
| 3.1.10 | 13.44 m^2 | 4 Outlets | 0                                     |

**Tabela de Materiais:**

![TabelaDeMateriaisPiso1](TabelaDeMateriaisPiso1.PNG)





#Explicação da Seleção dos Materiais Usados

* Temos 68 outlets, 5 **CPs** e 5 **MUTOAs** vai-se precisar
no minimo de 68 cabos CAT6. Usou-se **CPs** de 24 portas para
cobrir um par de salas exceto as salas 3.1.10 que tem um
**CP** de 12 portas e também a sala 3.1.9 que também te um **CP** de 12
portas 


* Decidiu-se seguir a regra em que deve-se deixar pelo menos 1/3 ou
metade das portas dos **CPs** livres.


* Colocou-se um **MUTOA** nas salas: 3.1.1,3.1.2,3.1.8 e 3.1.9 uma vez que existe uma área ampla no meio da sala 
e assumindo que haverá um elevado número de utilizadores nestas salas,  usou-se calhas
para esconder e organizar os cabos, sendo esta colada ao chão.


* O cabo **CAT7** é utilizado para conectar os **CPs**,**HC** e o **AP** entre eles, permitindo
assim um alto nível de tráfego de dados.Para alimentação dos AP o cabo CAT7 irá utilizar a tecnologia POE para alimentar de energia elétrica os equipamentos. Irão ser utilizados Power Injectors para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do HC para assim alimentar a ligação.


* Usou-se calhas para que certos outlets pudessem ser colocadas no meio da sala para
que os utilizadores pudessem aceder ás outlets numa distância máxima de 2 metros.

* A equipa achou pertinente utilizar cabos CAT7 entre o HC e os APs representados no sketch, pois este 
permite um alto nível de tráfego de dados.


* Para ligarmos os **MUTOAs**, é necessário alimentá-los 
com cabos de cobre **CAT7**. Estes vão sair do **HC** e 
ligar-se diretamente aos **MUTOAs**, uma vez que 
precisam de um alto nível de tráfego de dados (usando, por exemplo, o MUTOA: "MINI -C OM ® MuTOA 6 Port 
Outlet Box").


* Vão existir cabos a percorrer calhas que se encontram no teto falso, 
o qual cobre por completo todo o andar.

#Últimas observações

* Para a distribuição dos outlets de forma estruturada, seguiu-se a seguinte regra: "**A localização das outletss nas salas de trabalho deve ser tal que o equipamento do utilizar estejas ao alcance usando os patch cords de até no máximo cinco metros de comprimento e também fornecem flexibilidade para que os utilizadores possam deslocar os seus equipamentos. 
Indepedentemente onde esteja o equipamento do utilizador, é obrigatório haver uma tomada a menos de três metros de distância**".


* Para a colocação dos **CPs** usou-se a seguinte regras: "**Para os **CPs** é recomendado deixar pelo menos 1/3 das portas livres**".


* Para além dos PNGs da planta com o equipamento, também está disponibilizados SVGs dos mesmos para
que fornecem uma melhor qualidade de imagem.