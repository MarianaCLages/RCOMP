RCOMP 2021-2022 Project - Sprint 1 - Member 1200902 folder
===========================================

### <p> Durante a realização do **Sprint 1** do trabalho de **RCOMP**, foram desenvolvidos os sketches abaixo e as suas devidas explicações, que ilustram uma possível solução de cablagem (e respetivos equipamentos eletrónicos) que cobre por completo o **edifício 2**. Esta solução foi discutida em grupo para um melhor entendimento do mesmo.</p>

### Este edifício apresenta 18 salas no total, 6 no piso 0 e 12 no piso 1. Cada piso contém 2 WC, onde não vão ser necessários outlets, tal como especificado no enunciado do projeto. O edifício tem 20 metros de comprimento e 20 metros de largura, dando, assim, uma área de 400 metros quadrados no total. Seguem-se os sketches referidos e, a seguir, uma breve explicação dos mesmos.


#  ***Floor 0***

![B2_F0](B2_F0_Cabling.png)


## *Notas*

* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que eles estão colocados junto à mesma. Já os cabos paralelos à porta significa que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** e os **MUTOAs** que se encontram no meio da sala, é utilizada calha para cobrir os cabos que vão até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP**, o mesmo é ilustrado no sketch por um círculo a linha tracejada.


## *Informações*

| Sala     | Área      | Outlets    | CP  |
|:---------|:----------|:-----------|:----|
| 2.0.1 TR | 10.8 m^2  | 0 Outlets  | 0   |
| 2.0.2 WS | 30,71 m^2 | 8 Outlets  | 1   |
| 2.0.3 WS | 86 m^2    | 18 Outlets | 1   |
| 2.0.4 WS | 28.38 m^2 | 6 Outlets  | 0   |
| 2.0.5 WS | 28.38 m^2 | 6 Outlets  | 1   |
| 2.0.6 WS | 28.38 m^2 | 6 Outlets  | 0   |

**Nota:** A sala 2.0.1 é, tal como mencionado no enunciado do projeto, uma storage area e, por isso, não necessita de nenhum outlet.

- WS - Work Station
- TR - Telecommunication Room


### *Inventário do piso*

* **Sala 2.0.1 TR**

        1 MC (Main Cross-Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            2 Patch Cords (1 IC)

        1 IC (Intermediate Cross-Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            4 Patch Cords (1 HC piso 0 + 1 HC piso 1)

        1 HC (Horizontal Cross-Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            7 Patch Cords (3 CPs + 2 APs + 2 MUTOAs)

        1 Router
        TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.0.2 WS**

         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.0.3 WS**

        1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            18 Patch Cords (18 outlets)

        2 MUTOAs
        TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.0.5 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            18 Patch Cords (18 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* 44 **outlets**
* 2 Access-points (**AP**)
* 2,8(+) metros de cabo de **fibra ótica multivalor**
* XXX metros de cabo de cobre **CAT6**
* 110,4 metros de cabo de cobre **CAT7**
* 2 **Power Injectors**
* 2 **MUTOAs**
* 4 **TEs**


### *Observações e Implementações*

* Como temos 44 **outlets**, 2 **APs**, 3 **CPs**, 1 **MC**, 1 **IC**, 1 **HC** e 2 **MUTOAs** neste piso,
  vamos precisar, no mínimo, de 44 cabos de cobre (**CAT6**), 7 cabos de cobre (**CAT7**) e 6 cabos de **fibra ótica multivalor**. Visto que temos um **HC** com um **switch** de 12 portas (do tipo **CAT7**), vamos precisar de 3 **CPs**. Assim, as salas 2.0.3 e 2.0.5 possuem 1 CP com um switch de 24 portas, enquanto que a sala 2.0.2 possui 1 switch de apenas 12 portas, por forma a conseguirmos fazer as distribuições das tomadas pelas várias salas de forma organizada e estruturada.


* Apliquei a **redundância** com a utilização de 2 cabos de **fibra ótica multivalor** na ligação entre o **IC** e o **HC** deste piso, por forma a garantir o **balanceamento de carga**.
  O mesmo se aplica entre o **MC** e o **IC** que se encontram na sala 2.0.1, fazendo, assim, estas ligações diretas entre os dois sem haver cabos **desnecessariamente longos** (caso os cabos tivessem sido colocados noutro sítio, teriam de ser muito mais longos, gastando, assim, menos cabo de fibra).


* O **CP** da sala 2.0.5 vai alimentar tanto os outlets da própria sala como os outlets das salas 2.0.4 e 2.0.6, utilizando, assim, 18 portas do switch, o qual possui 24 portas no total e, portanto, ficam a sobrar 6 portas, o que permite possíveis melhorias futuras.


* No caso das salas 2.0.2 e 2.0.3, cada uma delas apresenta 1 **CP** que vai ficar encarregue de alimentar os outlets respetivos de cada uma das salas. No caso da sala 2.0.2, vão ser utilizadas 9 portas do switch de 12 portas, sobrando, assim, 3 portas e, no caso da sala 2.0.3, vão ser utilizadas 19 portas do switch de 24 portas sobrando, assim, 5 portas. Ambas as salas apresentam outlets em sobra, que vão possibilitar, se necessário no futuro, possíveis melhorias.


* Neste piso, foram ainda usados 2 **MUTOAs**, mais precisamente na sala 2.0.3, visto que existe **uma área ampla no meio da sala** e o mesmo permite uma distribuição mais organizada pelo espaço, permitindo que bastantes utilizadores que se encontrem no meio da sala tenham um outlet perto de si.


* Para ligarmos os **MUTOAs**, é necessário alimentá-los com cabos de cobre **CAT7**. Estes vão sair do **HC** e ligar-se diretamente aos **MUTOAs**, uma vez que precisam de um **alto nível de tráfego de dados** e, até porque estes vão apresentar 6 outlets (usando, por exemplo, o **MUTOA:** *"MINI -C OM ® MuTOA 6 Port Outlet Box"*).


* Utilizei cabos de **fibra ótica multivalor** até ao **HC**, uma vez que o seu comprimento não justifica a utilização de cabos de **fibra ótica monomodo** (o que seria uma melhor opção no caso de os cabos que estivessem a ser utilizados tivessem um comprimento superior a 1KM e, também, porque os mesmos são imunes à **dispersão** devido ao raio do seu núcleo ser tão pequeno) e, portanto, permite **taxas de dados altas**, até porque o **HC** é o fim do **Backbone**, ou seja, é ele que fica responsável pelo piso.
  A partir do **HC**, utilizei apenas cabos de cobre **CAT6** e cabos de cobre **CAT7** na distribuição do piso. Foram utilizados, respetivamente, cabos **CAT7** entre o **HC** e os 2 **APs**, para os 2 **MUTOAs** que se encontram neste piso e, também, entre a ligação do **HC** e os 3 **CPs**. Os cabos **CAT6** foram utilizados entre os **CPs** e os **outlets**.


* Na ligação de uma **Entidade Externa** (EF), consideramos que um cabo **ISP** é suficiente e que se vai conectar diretamente ao **MC** do edifício. Nesta conexão é aplicada redudância, por forma a garantir o **balanceamento de carga**.


* Achei pertinente utilizar cabos **CAT7** entre o **HC** e os **APs** representados no sketch, pois este permite um **alto nível de tráfego de dados**.


* Devido às paredes de betão armado deste edifício, temos de ter em consideração que o raio de alcance de cada **AP** é reduzido por volta de 10-20 metros, o que faz com que sejam necessários **2 APs** no mesmo piso para ficar completamente coberto por ‘wireless’.


* Para alcançar tanto os **outlets** como os **MUTOAs** que se encontram no meio da sala, é utilizada calha para esconder e organizar os cabos, sendo esta colada ao chão (e, caso necessário, podem existir tomadas elétricas nesta mesma calha).


* Os **APs** deste andar foram distribuídos de modo a cobrir o máximo espaço possível com ‘wireless’ do piso 0 e, possívelmente, entrada e arredores.
  No sketch do piso 0, os **APs** encontram-se colocados de forma simétrica relativamente aos do piso 1, possibilitando, assim, o máximo de cobertura possível com apenas 4 **APs** no total.


* Para a alimentação dos **APs**, o cabo **CAT7** irá utilizar a tecnologia **PoE** (Power over Ethernet). Irão ser utilizados **Power Injectors** para permitir ao cabo o transporte de energia elétrica. Estes dispositivos irão ser colocados na saída do **HC**, para alimentar a ligação.


* Todos os **patch cords** seguem a regra de terem um comprimento entre **0,5 e 5 metros**.


* o **HC** foi colocado na sala 2.0.1, pois, tal como mencionado no enunciado, esta sala é uma storage area e, neste caso, o **HC** permite uma melhor estruturação da rede e é uma forma de evitar cabos demasiado longos.


* Na maioria das salas vão existir cabos a percorrer calhas subterrâneas já implementadas no edifício.


* No mesmo **TE** em que se encontra o **MC** (sala 2.0.1) é onde se localiza o router de todo o edifício.



#  ***Floor 1***

![B2_F1](B2_F1_Cabling.png)


## *Notas*

* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que elas estão colocadas na mesma. Já os cabos representados paralelos à porta significam que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** e os **MUTOAs** que se encontram no meio da sala, é utilizada calha para cobrir os cabos que vão até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP**, o mesmo é ilustrado no sketch por um círculo a linha tracejada.


* **Nota 4:** É mencionado, no enunciado do projeto, que existe **teto falso em todo este piso**, colocado a 2,5 metros do chão, e que facilita a **cablagem** e a sua **estruturação**. 


## *Informações*

| Sala      | Área      | Outlets   | CP  |
|:----------|:----------|:----------|:----|
| 2.1.1 TR  | 10,8 m^2  | 0 Outlets | 0   |
| 2.1.2 WS  | 15,6 m^2  | 4 Outlets | 1   |
| 2.1.3 WS  | 15,6 m^2  | 4 Outlets | 0   |
| 2.1.4 WS  | 11,7 m^2  | 4 Outlets | 0   |
| 2.1.5 WS  | 11,7 m^2  | 4 Outlets | 1   |
| 2.1.6 WS  | 17,16 m^2 | 4 Outlets | 0   |
| 2.1.7 WS  | 20,79 m^2 | 6 Outlets | 1   |
| 2.1.8 WS  | 20,79 m^2 | 6 Outlets | 0   |
| 2.1.9 WS  | 15,6 m^2  | 4 Outlets | 1   |
| 2.1.10 WS | 15,6 m^2  | 4 Outlets | 0   |
| 2.1.11 WS | 15,6 m^2  | 4 Outlets | 0   |
| 2.1.12 WS | 18,72 m^2 | 4 Outlets | 1   |

WS - Work Station
TR - Telecommunication Room

**Nota:** A sala 2.1.1 é, tal como mencionado no enunciado do projeto, uma storage area e, por isso, não necessita de nenhum outlet.


### *Inventário do piso*

* **Sala 2.1.1 TR**

         1 HC (Horizontal Cross-Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            7 Patch Cords (5 CPs + 2 APs)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.1.2 WS**

         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.1.5 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            12 Patch Cords (12 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 2.1.7 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            12 Patch Cords (12 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão


* **Sala 2.1.9 WS**

         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão


* **Sala 2.1.12 WS**

         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* 48 **outlets**
* 2 Access-points (**AP**)
* 0,3 metros de cabo de **fibra ótica multivalor**
* 214,1 metros de cabo de cobre **CAT6**
* 156 metros de cabo de cobre **CAT7**
* 2 **Power Injectors**
* 6 **TEs**


### *Observações e Implementações*

* Como temos 48 **outlets**, 2 **APs**, 5 **CPs** e 1 **HC** neste piso, vamos precisar de, no mínimo, 48 cabos de cobre **CAT6**, 7 cabos de cobre **CAT7** e 2 cabos de **fibra ótica multivalor**. Sendo que temos um **HC** com 1 **switch** de 12 portas (do tipo **CAT7**), vamos precisar de 5 **CPs**. Assim, as salas 2.1.5 e 2.1.7 possuem 1 **CP** com um **switch** de 24 portas, enquanto que todas as outras salas onde existem **CPs**, possuem 1 **switch** de 12 portas, por forma a conseguirmos fazer as distribuições das tomadas pelas várias salas de forma organizada e estruturada.


* Apliquei a **redundância** com a utilização de 2 cabos de **fibra ótica multivalor** na ligação entre o **IC** (do piso 0) e o **HC**, por a garantir o **balanceamento de carga**, vindo estes cabos do piso 0.

