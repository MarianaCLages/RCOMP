RCOMP 2021-2022 Project - Sprint 1 - Member 1201487 folder
=========================================

### <p> Durante a realização do **Sprint 1** do trabalho de **RCOMP**, foram desenvolvidos os sketches abaixo e as suas devidas explicações, que ilustram uma possível solução de cablagem (e respetivos equipamentos eletrónicos) que cobre por completo o **edifício 4**. Esta solução foi discutida em grupo para um melhor entendimento do mesmo.</p>

### Este edifício apresenta 14 salas no total, 7 salas no piso 0 e outras 7 no piso 1. Cada piso contém 2 WC, onde não vão ser necessários outlets, tal como especificado no enunciado do projeto. O edifício tem 20 metros de comprimento e 20 metros de largura, dando, assim, uma área de 400 metros quadrados no total. Seguem-se os sketches referidos e, a seguir, uma breve explicação dos mesmos.


#  ***Floor 0***

![Floor0_Building4](Floor0_Building4.png)


## *Notas*

* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que eles estão colocados junto à mesma. Já os cabos paralelos à porta significa que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** e os **MUTOAs** que se encontram no meio da sala, é utilizada calha para cobrir os cabos que vão até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP**, o mesmo é ilustrado no sketch por um círculo a linha tracejada.


## *Informações*

| Sala     | Área      | Outlets    | CP  |
|:---------|:----------|:-----------|:----|
| 4.0.1 WS | 53,44 m^2 | 12 Outlets | 1   |
| 4.0.2 WS | 30,81 m^2 | 8 Outlets  | 1   |
| 4.0.3 WS | 30,81 m^2 | 8 Outlets  | 0   |
| 4.0.4 WS | 58,44 m^2 | 12 Outlets | 1   |
| 4.0.5 TR | 7,74 m^2  | 0 Outlets  | 0   |
| 4.0.6 WS | 14,63 m^2 | 4 Outlets  | 1   |
| 4.0.7 WS | 13,81 m^2 | 4 Outlets  | 0   |

**Nota:** A sala 4.0.5 é, tal como mencionado no enunciado do projeto, uma storage area e, por isso, não necessita de nenhum outlet.

- WS - Work Station
- TR - Telecommunication Room


### *Inventário do piso*

* **Sala 4.0.1 WS**
  
         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            6 Patch Cords (6 outlets)

         1 MUTOA
         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.0.2 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            16 Patch Cords (16 outlets)
  
         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.0.4 WS**

        1 MC (Main Cross Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            2 Patch Cords (1 IC)

        1 IC (Intermediate Cross Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            4 Patch Cords (1 HC piso 0 + 1 HC piso 1)

        1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)
  
        1 Router ??
        1 MUTOA
        TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.0.5 TR**

         1 HC (Horizontal Cross Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            8 Patch Cords (4 CPs + 2 APs + 2 MUTOAs)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.0.6 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            10 Patch Cords (10 outlets)
  
         TE (Telecommunication Enclosure) - XXX dimensão

* 48 **outlets**
* 2 Access-points (**AP**) 
* XXX metros de cabo de **fibra ótica multivalor**
* XXX metros de cabo de cobre **CAT6**
* XXX metros de cabo de cobre **CAT7**
* 2 **Power Injectors**
* 2 **MUTOAs**
* 5 **TEs**


### *Observações e Implementações*

* Como temos 48 **outlets**, 2 **APs**, 4 **CPs**, 1 **MC**, 1 **IC**, 1 **HC** e 2 **MUTOAs** neste piso, 
  vamos precisar, no mínimo, de 48 cabos de cobre (**CAT6**), 8 cabos de cobre (**CAT7**) e 6 cabos de **fibra ótica multivalor**. Visto que temos um **HC** com um **switch** de 12 portas (do tipo **CAT7**), vamos precisar de 4 **CPs**. Assim, as salas 4.0.1 e 4.0.4 possuem 1 CP com um switch de 12 portas, enquanto que todas as outras salas onde existem CPs, possuem 1 switch de 24 portas, por forma a conseguirmos fazer as distribuições das tomadas pelas várias salas de forma organizada e estruturada.
  

* Apliquei a **redundância** com a utilização de 2 cabos de **fibra ótica multivalor** na ligação entre o **IC** e o **HC** deste piso, por forma a garantir o **balanceamento de carga**.
 O mesmo se aplica entre o **MC** e o **IC** que se encontram na sala 4.0.4, fazendo, assim, estas ligações diretas entre os dois sem haver cabos **desnecessariamente longos** (caso os cabos tivessem sido colocados noutro sítio, teriam de ser muito mais longos, gastando, assim, menos cabo de fibra).
 

* O **CP** da sala 4.0.6 vai alimentar tanto os outlets da própria sala como os outlets da sala 4.0.7, utilizando, assim, 10 portas do switch, o qual possui 24 portas no total e, portanto, ficam a sobrar 14 portas, o que permite possíveis melhorias futuras.


* O **CP** da sala 4.0.3 vai alimentar tanto os outlets da própria sala como os outlets da sala 4.0.2, utilizando, assim, 16 portas do switch, o qual possui 24 portas no total e, portanto, ficam a sobrar 8 portas, o que permite possíveis melhorias futuras.


* No caso das salas 4.0.1 e 4.0.4, cada uma delas apresenta 1 **CP** que vai ficar encarregue de alimentar os outlets respetivos de cada uma das salas. No caso da sala 4.0.1, vão ser utilizadas 6 portas do switch de 12 portas, sobrando, assim, 6 portas e, no caso da sala 4.0.4, vão ser utilizadas 8 portas do switch de 12 portas sobrando, assim, 4 portas. Ambas as salas apresentam outlets em sobra, que vão possibilitar, se necessário no futuro, possíveis melhorias.


* Neste piso, foram ainda usados 2 **MUTOAs**, mais precisamente nas salas 4.0.1 e 4.0.4, visto que existe **uma área ampla no meio da sala** e o mesmo permite uma distribuição mais organizada pelo espaço, permitindo que bastantes utilizadores que se encontrem no meio da sala tenham um outlet perto de si.


* Para ligarmos os **MUTOAs**, é necessário alimentá-los com cabos de cobre **CAT7**. Estes vão sair do **HC** e ligar-se diretamente aos **MUTOAs**, uma vez que precisam de um **alto nível de tráfego de dados** e, até porque estes vão apresentar 6 outlets (usando, por exemplo, o **MUTOA:** *"MINI -C OM ® MuTOA 6 Port Outlet Box"*).


* Utilizei cabos de **fibra ótica multivalor** até ao **HC**, uma vez que o seu comprimento não justifica a utilização de cabos de **fibra ótica monomodo** (o que seria uma melhor opção no caso de os cabos que estivessem a ser utilizados tivessem um comprimento superior a 1KM e, também, porque os mesmos são imunes à **dispersão** devido ao raio do seu núcleo ser tão pequeno) e, portanto, permite **taxas de dados altas**, até porque o **HC** é o fim do **Backbone**, ou seja, é ele que fica responsável pelo piso.
  A partir do **HC**, utilizei apenas cabos de cobre **CAT6** e cabos de cobre **CAT7** na distribuição do piso. Foram utilizados, respetivamente, cabos **CAT7** entre o **HC** e os 2 **APs**, para os 3 **MUTOAs** que se encontram neste piso e, também, entre a ligação do **HC** e os 4 **CPs**. Os cabos **CAT6** foram utilizados entre os **CPs** e os **outlets**.

 
* Na ligação de uma **Entidade Externa** (EF), consideramos que um cabo **ISP** é suficiente e que se vai conectar diretamente ao **MC** do edifício. Nesta conexão é aplicada redudância, por forma a garantir o **balanceamento de carga**.


* Achei pertinente utilizar cabos **CAT7** entre o **HC** e os **APs** representados no sketch, pois este permite um **alto nível de tráfego de dados**.


* Devido às paredes de betão armado deste edifício, temos de ter em consideração que o raio de alcance de cada **AP** é reduzido por volta de 10-20 metros, o que faz com que sejam necessários **2 APs** no mesmo piso para ficar completamente coberto por ‘wireless’.


* Para alcançar tanto os **outlets** como os **MUTOAs** que se encontram no meio da sala, é utilizada calha para esconder e organizar os cabos, sendo esta colada ao chão (e, caso necessário, podem existir tomadas elétricas nesta mesma calha).


* Os **APs** deste andar foram distribuídos de modo a cobrir o máximo espaço possível com ‘wireless’ do piso 0 e, possívelmente, entrada e arredores.
 No sketch do piso 0, os **APs** encontram-se colocados de forma simétrica relativamente aos do piso 1, possibilitando, assim, o máximo de cobertura possível com apenas 4 **APs** no total.


* Para a alimentação dos **APs**, o cabo **CAT7** irá utilizar a tecnologia **POE** (Power over Ethernet). Irão ser utilizados **Power Injectors** para permitir ao cabo o transporte de energia elétrica. Estes dispositivos irão ser colocados na saída do **HC**, para alimentar a ligação.


* Todos os **patch cords** seguem a regra de terem um comprimento entre **0,5 e 5 metros**.


* o **HC** foi colocado na sala 4.0.5, pois, tal como mencionado no enunciado, esta sala é uma storage area e, neste caso, o **HC** permite uma melhor estruturação da rede e é uma forma de evitar cabos demasiado longos.


* Na maioria das salas vão existir cabos a percorrer calhas subterrâneas já implementadas no edifício.


* No mesmo **TE** em que se encontra o **MC** (sala 4.0.4) é onde se localiza o router de todo o edifício.



#  ***Floor 1***

![Floor1_Building4](Floor1_Building4.png)


## *Notas*

* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que elas estão colocadas na mesma. Já os cabos representados paralelos à porta significam que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** e os **MUTOAs** que se encontram no meio da sala, é utilizada calha para cobrir os cabos que vão até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP**, o mesmo é ilustrado no sketch por um círculo a linha tracejada.


* **Nota 4:** É mencionado, no enunciado do projeto, que existe **teto falso em todo este piso**, colocado a 2,5 metros do chão, e que facilita a **cablagem** e a sua **estruturação**. 


## *Informações*

| Sala     | Área      | Outlets    | CP  |
|:---------|:----------|:-----------|:----|
| 4.1.1 WS | 81,26 m^2 | 18 Outlets | 1   |
| 4.1.2 WS | 32,8 m^2  | 8 Outlets  | 1   |
| 4.1.3 WS | 27,17 m^2 | 6 Outlets  | 0   |
| 4.1.4 WS | 28,98 m^2 | 6 Outlets  | 0   |
| 4.1.5 WS | 27,17 m^2 | 6 Outlets  | 1   |
| 4.1.6 TR | 7,40 m^2  | 0 Outlets  | 0   |
| 4.1.7 WS | 51,85 m^2 | 12 Outlets | 1   |

WS - Work Station
TR - Telecommunication Room

**Nota:** A sala 4.1.6 é, tal como mencionado no enunciado do projeto, uma storage area e, por isso, não necessita de nenhum outlet.


### *Inventário do piso*

* **Sala 4.1.1 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         2 MUTOAs
         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.1.2 WS**

         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            15 Patch Cords (15 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.1.5 WS**
  
         1 CP (Consolidation Point):
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            12 Patch Cords (12 outlets)
  
         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.1.6 TR**

         1 HC (Horizontal Cross Connect):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            9 Patch Cords (4 CPs + 2 APs + 3 MUTOAs)

         TE (Telecommunication Enclosure) - XXX dimensão

* **Sala 4.1.7 WS**

         1 CP (Consolidation Point):
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

         TE (Telecommunication Enclosure) - XXX dimensão

* 56 **outlets**
* 2 Access-points (**AP**)
* XXX metros de cabo de **fibra ótica multivalor**
* XXX metros de cabo de cobre **CAT6**
* XXX metros de cabo de cobre **CAT7**
* 2 **Power Injectors**
* 3 **MUTOAs**
* 5 **TEs**


### *Observações e Implementações*

* Como temos 56 **outlets**, 2 **APs**, 4 **CPs**, 1 **HC** e 3 **MUTOAs** neste piso, vamos precisar de, no mínimo, 56 cabos de cobre **CAT6**, 9 cabos de cobre **CAT7** e 2 cabos de **fibra ótica multivalor**. Sendo que temos um **HC** com 1 **switch** de 12 portas (do tipo **CAT7**), vamos precisar de 4 **CPs**. Assim, a sala 4.1.7 possui 1 **CP** com um **switch** de 12 portas, enquanto que todas as outras salas onde existem **CPs**, possuem 1 **switch** de 24 portas, por forma a conseguirmos fazer as distribuições das tomadas pelas várias salas de forma organizada e estruturada.


* Apliquei a **redundância** com a utilização de 2 cabos de **fibra ótica multivalor** na ligação entre o **IC** (do piso 0) e o **HC**, por a garantir o **balanceamento de carga**, vindo estes cabos do piso 0.


* Coloquei o **HC** na sala 4.1.6, porque é mencionado no enunciado do projeto que esta seria uma boa sala para tal e, também, para ser possível uma melhor estruturação da rede neste piso (visto que é uma forma de evitar cabos demasiado longos).


* O **CP** da sala 4.1.2 vai alimentar tanto os outlets da própria sala como os outlets da sala 4.1.4, utilizando, assim, 15 portas do switch, o qual possui 24 portas no total e, portanto, ficam a sobrar 9 portas, o que permite possíveis melhorias futuras.


* O **CP** da sala 4.1.5 vai alimentar tanto os outlets da própria sala como os outlets da sala 4.1.3, utilizando, assim, 12 portas do switch, o qual possui 24 portas no total e, portanto, ficam a sobrar 12 portas, o que permite possíveis melhorias futuras.


* No caso das salas 4.1.1 e 4.1.7, cada uma delas apresenta 1 **CP** que vai ficar encarregue de alimentar os outlets respetivos de cada uma das salas. No caso da sala 4.1.1. vão ser utilizadas 8 portas do switch de 24 portas, sobrando, assim, 16 portas e, no caso da sala 4.1.7, vão ser utilizadas 8 portas do switch de 12 portas, sobrando, assim, 4 portas. Ambas as salas apresentam outlets em sobra, que vão possibilitar, se necessário no futuro, possíveis melhorias.
Optei neste caso por utilizar um patch panel na sala 4.1.1 com 24 portas enquanto que na sala 4.1.7 utilize um de 12 portas, uma vez que, a sala 4.1.1 é muito maior do que a sala 4.1.7 o que significa que poderá ser necessário mais outlets do que a regra geral naquela sala, possibilitanto assim essa transição e melhoria.

  
* Neste piso, foram ainda usados 3 **MUTOAs**, mais precisamente, nas salas 4.1.1 e 4.1.7, visto que existe **uma área ampla no meio da sala** e o mesmo permite uma distribuição mais organizada pelo espaço, permitindo que bastantes utilizadores que se encontrem no meio da sala tenham um outlet perto de si.


* Para ligarmos os **MUTOAs**, é necessário alimentá-los com cabos de cobre **CAT7**. Estes vão sair do **HC** e ligar-se diretamente aos **MUTOAs**, uma vez que precisam de um **alto nível de tráfego de dados** e, até porque estes vão apresentar 6 outlets (usando, por exemplo, o **MUTOA**: *"MINI -C OM ® MuTOA 6 Port Outlet Box"*).


* Utilizei cabos de **fibra ótica multivalor** até ao **HC**, uma vez que o seu comprimento não justifica a utilização de cabos de **fibra ótica monomodo** (o que seria uma melhor opção no caso de os cabos que estivessem a ser utilizados tivessem um comprimento superior a 1KM e, também, porque os mesmos são imunes à **dispersão** devido ao raio do seu núcleo ser tão pequeno) e, portanto, permite **taxas de dados altas**, até porque o **HC** é o fim do **Backbone**, ou seja, é ele que fica responsável pelo piso.
  A partir do **HC**, utilizei apenas cabos de cobre **CAT6** e cabos de cobre **CAT7** na distribuição do piso. Foram utilizados, respetivamente, cabos **CAT7** entre o **HC** e os 2 **APs**, para os 3 **MUTOAs** que se encontram neste piso e, também, entre a ligação do **HC** e os 4 **CPs**. Os cabos **CAT6** foram utilizados entre os **CPs** e os **outlets**.

  
* Achei pertinente utilizar cabos **CAT7** entre o **HC** e os **APs** representados no sketch, pois este permite um **alto nível de tráfego de dados**.


* Devido às paredes de betão armado deste edifício, temos de ter em consideração que o raio de alcance de cada **AP** é reduzido por volta de 10-20 metros, o que faz com que sejam necessários **2 APs** no mesmo piso para ficar completamente coberto por ‘wireless’.


* Para alcançar tanto os **outlets** como os **MUTOAs** que se encontram no meio da sala, é utilizada calha para esconder e organizar os cabos, sendo esta colada ao chão (e, caso necessário, podem existir tomadas elétricas nesta mesma calha);


* Os **APs** deste andar foram distribuídos de modo a cobrir o máximo espaço possível com ‘wireless’ do piso 1 e, possivelmente, entrada e arredores.
  No sketch do piso 1, os **APs** encontram-se colocados de forma simétrica relativamente aos do piso 0, possibilitando, assim, o máximo de cobertura possível com apenas 4 **APs** no total.


* Para a alimentação dos **APs**, o cabo **CAT7** irá utilizar a tecnologia **PoE** (Power over Ethernet). Irão ser utilizados **Power Injectors** para permitir ao cabo o transporte de energia elétrica. Estes dispositivos irão ser colocados na saída do **HC**, para alimentar a ligação.


* Todos os **patch cords** seguem a regra de terem um comprimento entre **0,5 e 5 metros**.


* Na maioria das salas, tal como mencionado numa nota debaixo do sketch, vão existir cabos a percorrer calhas que se encontram no teto falso, o qual cobre por completo todo o andar.


## **Cálculos e finais observações**

* Para determinar o número de outlets necessários para cada divisão, baseei-me na seguinte regra: **"Os padrões de cabeamento estruturado especificam um mínimo de duas saídas por área de trabalho, também duas saídas para cada 10 metros quadrados de área. Portanto, para uma área de trabalho acima de 10 m^2, quatro saídas devem estar disponíveis."**.


* Na distribuição dos outlets de forma estruturada, segui a seguinte regra: **"A localização das tomadas dentro da área de trabalho deve ser tal que o equipamento do usuário final
  está ao alcance usando os patch cords de até cinco metros de comprimento e também fornecem
  flexibilidade para que os usuários possam mover os seus equipamentos. Onde quer que o usuário
  equipamento é, deve haver sempre uma tomada a menos de três metros de distância."**.
  
  
* Em relação à redundância de cabos do backbone, segui e implementei esta regra: **"Cada conexão de backbone deve ser um conjunto de vários cabos paralelos. Este conjunto
  de vários cabos pode ser usado de várias maneiras:
  Use um único, se algum dia falhar, o operador pode alternar para outro
  Isso é chamado de failover (neste caso, failover manual).
  O mesmo de antes, mas automático. Usando os protocolos apropriados, a camada 2
  (comutação) e os dispositivos de camada 3 (roteamento) detectam se um cabo está falhando e
  alternar automaticamente para outro.
  O mesmo que antes, mas todos os cabos alternativos são usados ao mesmo tempo para
  transmitir dados com balanceamento de carga. Isso não é mais chamado de failover, mas se um
  cabo falhar, ele não será mais usado."**. Ou até mesmo, a seguinte informação que consta na PL1: **"Conexões redundantes de cabos de backbone são desejáveis, elas fornecem tolerância a falhas (failover) e também podem
  ser usadas para aumentar a largura de banda (balanceamento de carga de rede). No que diz respeito a cabos redundantes, estes
  recursos podem ser habilitados posteriormente nos switches da camada dois (Spanning Tree Protocol e Link Aggregation
  Control Protocol) ou nos roteadores da camada três (Dynamic Routing Protocols)."**.
  

* Em relação aos **TEs**, segui tanto esta regra: **"Each cross-connect will have at least one
telecommunication enclosure. Rack enclosures vertical size is measured in
U rack units (1.75’’/44.45 mm). Typical CAT7 24 ports patch panels have 1U
size. Defining the enclosure size reflects what we already know: the patch
panels that will be fitted there, but that’s not enough, active equipment will
also be placed there."**, como também: **"One thing to bear in mind is that these enclosures will house not
only the wiring termination hardware but also active equipment
that is not part of the cabling system itself like switches, routers,
servers, UPS (Uninterruptible Power Supply), etc.
The exact size of telecommunications enclosures cannot be derived from the
cabling system only, it must also take in account space for other hardware.
Also, an up to 50% oversizing is wise to accommodate future upgrades."**.


* Para além dos ficheiros *.png* disponibilizados dos sketches do piso 0 e do piso 1, também foi disponibilizado o seu respetivo ficheiro *.svg*, no entanto, este revelou alguns problemas de formatação no momento em que foi exportado, por isso optei por utilizar os ficheiros *.png* na apresentação do markdown.


* Estão, também, disponibilizados os sketches com as medições tanto do piso 0 como do piso 1, uma vez que, no sketch total, algumas medições ficaram um pouco tapadas pelos cabos que por lá passavam.