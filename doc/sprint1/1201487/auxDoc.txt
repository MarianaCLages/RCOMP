RCOMP 2021-2022 Project - Sprint 1 - Member 1201487 folder
=========================================

### <p> Durante a realização do **Sprint 1** do trabalho de **RCOMP** foram desenvolvidos estes possíveis sketches, e devidas explicações, que ilustram uma possível solução de cabelagem (e respetivos equipamentos eletrónicos) que cobriam por completo o **edifício 4**. Esta solução foi discutida em grupo para um melhor entendimento entre o mesmo. Segue se, assim, os sketches referidos e a seguir uma breve explicação dos mesmos. </p>

#  ***Floor 0***
#

![Floor0_Building4](Floor0_Building4.png)

#

## *Notas:*

* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que elas estão colocadas na mesma. Já os cabos que estão representados paralelos à porta significam que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** ou **MUTOAs** que se encontram no meio da sala é utilizado calha para cobrir os cabos que são levados até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP** é ilustrado no sketch.
#

## *Informações:*

| Sala  | Área | Outlets | CP                                                                                   |
| :-------------    | :--------------------- | :------------ | :----------------------------                                                                            |
| 4.0.1 WS    | 53,44 m^2 | 12 Outlets | 1 |
| 4.0.2 WS    | 30,81 m^2 | 8 Outlets  | 1 |
| 4.0.3 WS    | 30,81 m^2 | 8 Outlets  | 0 |
| 4.0.4 WS    | 58,44 m^2 | 12 Outlets | 1 |
| 4.0.5 TR    | 7,74  m^2 | 0 Outlets  | 0 |
| 4.0.6 WS    | 14,63 m^2 | 4  Outlets | 1 |
| 4.0.7 WS    | 13,81 m^2 | 4 Outlets  | 0 |

**Nota** : A sala 4.0.5 é uma storagem area, tal como mencionado do enunciado do projeto, então não vai ser necessário nenhum outlet.

WS - Work Station 
TR - Telecomunication Room

### *Inventário do piso*

* **Sala 4.0.1 WS** :
  
         1 CP (Consolidation Point) :
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            6 Patch Cords (6 outlets)

        1 MUTOA
        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.0.2 WS** :

         1 CP (Consolidation Point) :
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            16 Patch Cords (16 outlets )
  
        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.0.4 WS** :

        1 MC (Main Cross Connect) :
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            2 Patch Cords (1 IC)

        1 IC (Intermidiate Cross Connect) :
            1 switch 12 portas
            1 Patch Panel 12 portas de fibra ótica - Multivalor
            4 Patch Cords (1 HC piso 0 + 1 HC piso 1)

         1 CP (Consolidation Point) :
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)
  
        1 Router ??
        1 MUTOA
        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.0.5 TR** :

         1 HC (Horizontal Cross Connect) :
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            8 Patch Cords (4 CPs + 2 APs + 2 MUTOA)

        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.0.6 WS** :

         1 CP (Consolidation Point) :
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            10 Patch Cords (10 outlets)
  
        TE (Telecomunication Enclosure) - XXX dimensão

* 48 **outlets**
* 2 Access-points (**AP**) 
* XXX metros de cabo de **fibra ótica multivalor**
* XXX metros de cabo de cobre - **CAT6**
* XXX metros de cabo de cobre - **CAT7**
* 2 **Power Injectors**
* 2 **MUTOAs**
* 5 **TEs**

### *Observações e Implementações*

* Como temos 48 outlets, 2 **APs**, 4 **CPs**, 1 **MC**, 1 **IC**, 1 **HC** 2 **MUTOAs**, neste piso, 
  vamos precisar no mínimo de 48 cabos de cobre - **CAT6**, 8 cabos de cobre - **CAT7** e 6 cabos de **fibra ótica multivalor**. Sendo que temos um **HC** com 1 **switch** de 12 portas (do tipo **CAT7**) vamos precisar de 4 **CPs**, existindo, no caso da sala 4.0.1 e da sala 4.0.4 1 **CP** com um **switch** de 12 portas enquanto em todas as outras salas onde existem **CPs** apresentam 1 **switch** de 24 portas para conseguirmos conseguir fazer as distribuições das tomadas pelas salas de forma organizada e estruturada.
  

* Apliquei a **redundância**, com a utilização de 2 cabos (**fibra óptica multivalor**), na ligação entre o **IC** o e **HC** para o **balanceamento de carga**, isto para o piso 0, pois de igual forma vai sair 2 cabos de **fibra ótica multivalor** para o **HC** do piso 1, aplicando, assim, aplicando **redundância** também.
 O mesmo vai se aplicar entre o **MC** e o **IC**, que se encontram ambos na sala 4.0.4 fazendo assim estas ligações diretas entre os dois sem haver cabos **descenessariamente longos** (caso tivesse sido colocado noutro sítio os cabos, neste caso, teriam de ser muito mais longo do que estão a ser neste momento, gastando assim menos cabo de fibra).
 

* O **CP** da sala 4.0.6 vai tanto alimentar os outlets da própria sala como os outlets da sala 4.0.7, utilizando assim no total, 10 portas do switch que apresenta 24 portas no total, sobrando assim 14 portas no total, permitindo assim possíveis futuras melhorias.


* O **CP** da sala 4.0.3 vai tanto alimentar os outlets da própria sala como os outlets da sala 4.0.2, utilizando assim no total, 16 portas do switch que apresenta 24 portas no total, sobrando assim 8 portas no total, permitindo assim possíveis futuras melhorias.


* No caso das salas 4.0.1 e 4.0.4, cada uma delas apresenta 1 **CP** que vai ficar encarregue de alimentar os outlets respetivos de cada sala. No caso da sala 4.0.1 vão ser utilizadas 6 portas do switch de 12 portas, sobrando assim 6 portas; e no caso da sala 4.0.4 vao ser utilizadas 8 portas do switch de 12 portas sobrando assim 4 portas. Tanto uma sala como a outra vão apresentar outlets a sobrar que vão possibilitar, no futuro se for necessário, possíveis melhorias.


* Para além disso, foram usados 2 **MUTOA** neste andar, precisamente, na sala 4.0.1 e na sala 4.0.4, uma vez que existe **uma área ampla no meio da sala** e o mesmo permite uma distribuição mais organizado no mesmo (permitindo assim bastantes utilizadores que se encontram no meio da sala tenham um outlet perto de si);


* Para ligarmos os **MUTOAs** vai ser necessário alimentar os mesmos com cabos **CAT7**. Os mesmos vão sair do **HC** e ligar diretamente os **MUTOAs**, uma vez que, estes precisam de um **alto nível de tráfego de dados** até porque estes vão apresentar 6 outlets (usando por exemplo o **Mutoa**: *"MINI -C OM ® MuTOA 6 Port Outlet Box"*)


* Utilizei Cabos de **fibra otica multivalor** até ao **HC**, uma vez que o comprimento dos cabos não justifica a utilização de cabos de **fibra ótica monomodo** (o que seria melhor caso os cabos que estariam a ser utilizados tivessem mais que 1KM, e uma vez que, os mesmos são imunes à **dispersão** devido ao raio do seu núcleo ser tão pequeno) e, portanto, permite **taxas de dados altas** até porque o **HC** é o fim do **Backbone**, ou seja é ele que fica responsável pelo piso.
  A partir do **HC** utilizei apenas cabos de cobre - **CAT6** e cabos de cobre - **CAT7** na distribuição do piso. Foram utilizados, respetivamente, cabos **CAT7** entre o **HC** e os 2 **APs** e os 3 **MUTOAs** que se encontram neste piso e também entre a ligação do **HC** e os 4 **CPs**, e cabos **CAT6** entre os **CPs** e os outlets.

 
* Na ligação de uma **Entidade Externa** (EF), estamos a considerar que chega um cabo **ISP** que vai se conectar diretamente ao **MC** do edifício é aplicado sobre esta conexeção redudância para o **balanceamento de carga**.


* Achei pretinente utilizar cabos **CAT7** entre o **HC** e os **AP** representados no sketch, pois o mesmo permite **alto nível de tráfego de dados**;


* Devido às paredes de betão armado que existem no piso, temos de ter em consideração o fator que o raio de alcance de cada **AP** é reduzido por volta de 10-20 metros, o que vai fazer com que seja necessário **2 APs** no mesmo piso para que fique completamente coberto por wireless;


* Para alcançar tanto os **outlets** como os **MUTOAs** que se encontram no meio da sala, é utilizado calha para esconder e organizar os cabos, sendo esta colada ao chão (e caso fosse necessário poderia existir tomadas elétricas nesta mesma calha);


* Os **APs** deste andar foram distribuídos do modo que conseguissem cobrir o máximo possível com wireless o piso 0 e possívelmente entrada e arredores.
 No sketch do piso 0 vai ser possível que os **APs** se encontram colocados respetivamente aos do piso 1 de uma forma simétrica possibilitando assim o máximo de cobertura possível com apenas 4 **APs** no total.


* Para alimentação dos **AP** o cabo **CAT7** irá utilizar a tecnologia **POE** para alimentar de energia elétrica os equipamentos. Irão ser utilizados **Power Injectors** para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do **HC** para assim alimentar a ligação.


* Todo os **patch cords** vão seguir a regra que tem de ter um comprimento entre **0.5 - 5 metros**.


* o **HC** foi colocado na sala 4.0.5 pois tal como mencionado no projeto a sala 4.0.5 é uma storage area e neste caso ficaria bem aqui o **HC** para permitir uma melhor estruturação da rede e evitar cabos desnecessariamente longos.


* Na maioria das salas, vai existir cabos a percorrer por calhas subterrâneas já implementada no edifício.


* No mesmo **TE** em que se encontra o **MC** (sala 4.0.4) vai se encontrar lá o router do edifício todo.


#  ***Floor 1***
#


![Floor1_Building4](Floor1_Building4.png)

#

## *Notas:*
* **Nota 1:** Os cabos representados **perto e paralelos à parede** representam cabos na parede **cobertos por calhas**, assim como os **outlets junto à parede** significam que elas estão colocadas na mesma. Já os cabos que estão representados paralelos à porta significam que a estão a **contornar**.


* **Nota 2:** Como é possível observar no sketch, para alcançar os **outlets** ou **MUTOAs** que se encontram no meio da sala é utilizado calha para cobrir os cabos que são levados até aos mesmos.


* **Nota 3:** Para uma melhor compreensão do alcance de cada **AP** é ilustrado no sketch.


* **Nota 4:** É mencionado no enunciado do projeto que existe **teto falso em todo este piso**, que vai facilitar a **cabelagem** neste andar e a **estruturação da mesma**. 
#

## *Informações:*

| Sala  | Área | Outlets | CP                                                                                   |
| :-------------    | :--------------------- | :------------ | :----------------------------                                                                            |
| 4.1.1 WS    | 81,26 m^2 | 18 Outlets | 1 |
| 4.1.2 WS    | 32,8 m^2 | 8 Outlets  | 1 |
| 4.1.3 WS    | 27,17 m^2 | 6 Outlets  | 0 |
| 4.1.4 WS    | 28,98 m^2 | 6 Outlets | 0 |
| 4.1.5 WS    | 27,17  m^2 | 6 Outlets  | 1 |
| 4.1.6 TR    | 7,40 m^2 | 0  Outlets | 0 |
| 4.1.7 WS    | 51,85 m^2 | 12 Outlets  | 1 |

WS - Work Station
TR - Telecomunication Room

**Nota** : A sala 4.1.6 é uma storagem area, tal como mencionado do enunciado do projeto, então não vai ser necessário nenhum outlet.

### *Inventário do piso*

* **Sala 4.1.1 WS** :

         1 CP (Consolidation Point) :
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

        2 MUTOA
        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.1.2 WS** :

         1 CP (Consolidation Point) :
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            15 Patch Cords (15 outlets )

        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.1.5 WS** :
  
         1 CP (Consolidation Point) :
            1 switch 24 portas
            1 Patch Panel 24 portas de cobre - CAT6
            12 Patch Cords (12 outlets)
  
        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.1.6 TR** :

         1 HC (Horizontal Cross Connect) :
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT7
            9 Patch Cords (4 CPs + 2 APs + 3 MUTOA)

        TE (Telecomunication Enclosure) - XXX dimensão

* **Sala 4.1.7 WS** :

         1 CP (Consolidation Point) :
            1 switch 12 portas
            1 Patch Panel 12 portas de cobre - CAT6
            8 Patch Cords (8 outlets)

        TE (Telecomunication Enclosure) - XXX dimensão

* 56 **outlets**
* 2 Access-points (**AP**)
* XXX metros de cabo de **fibra ótica multivalor**
* XXX metros de cabo de cobre - **CAT6**
* XXX metros de cabo de cobre - **CAT7**
* 2 **Power Injectors**
* 3 **MUTOAs**
* 5 **TEs**

### *Observações e Implementações*

* Como temos 56 outlets, 2 **APs**, 4 **CPs**, 1 **HC** 3 **MUTOAs**, neste piso,
  vamos precisar no mínimo de 56 cabos de cobre - **CAT6**, 9 cabos de cobre - **CAT7** e 2 cabos de **fibra ótica multivalor**. Sendo que temos um **HC** com 1 **switch** de 12 portas (do tipo **CAT7**) vamos precisar de 4 **CPs**, existindo, no caso da sala 4.1.7-  1 **CP** com um **switch** de 12 portas enquanto em todas as outras salas onde existem **CPs** apresentam 1 **switch** de 24 portas para conseguirmos conseguir fazer as distribuições dos outlets pelas salas de forma organizada e estruturada.


* Apliquei a **redundância**, com a utilização de 2 cabos (**fibra óptica multivalor**), na ligação entre o **IC**(do piso 0) e o **HC** para o **balanceamento de carga**, vindo estes cabos do piso 0.


* Coloquei o **HC** na sala 4.1.6, porque é mencionado no enunciado do projeto que seria uma boa sala para se localizar para ser possível uma melhor estruturação da rede neste piso (uma vez que vai evitar cabos desnecessariamente longos). 


* O **CP** da sala 4.1.2 vai tanto alimentar os outlets da própria sala como os outlets da sala 4.1.4, utilizando assim no total, 15 portas do switch que apresenta 24 portas no total, sobrando assim 9 portas no total, permitindo assim possíveis futuras melhorias.


* O **CP** da sala 4.1.5 vai tanto alimentar os outlets da própria sala como os outlets da sala 4.1.3, utilizando assim no total, 12 portas do switch que apresenta 24 portas no total, sobrando assim 12 portas no total, permitindo assim possíveis futuras melhorias.


* No caso das salas 4.1.1 e 4.1.7, cada uma delas apresenta 1 **CP** que vai ficar encarregue de alimentar os outlets respetivos de cada sala. No caso da sala 4.1.1 vão ser utilizadas 8 portas do switch de 24 portas, sobrando assim 16 portas; e no caso da sala 4.1.7 vao ser utilizadas 8 portas do switch de 12 portas sobrando assim 4 portas. Tanto uma sala como a outra vão apresentar outlets a sobrar que vão possibilitar, no futuro se for necessário, possíveis melhorias.
Optei neste caso por utilizar um patch panel na sala 4.1.1 com 24 portas enquanto que na sala 4.1.7 utilize um de 12 portas, uma vez que, a sala 4.1.1 é muito maior do que a sala 4.1.7 o que significa que poderá a vir a ser necessário mais outlets do que a regra geral naquela sala, possibilitanto assim essa transição e melhoria.

  
* Para além disso, foram usados 3 **MUTOA** neste andar, precisamente, na sala 4.1.1 e na sala 4.1.7, uma vez que existe **uma área ampla no meio da sala** e o mesmo permite uma distribuição mais organizado no mesmo (permitindo assim bastantes utilizadores que se encontram no meio da sala tenham um outlet perto de si);


* Para ligarmos os **MUTOAs** vai ser necessário alimentar os mesmos com cabos **CAT7**. Os mesmos vão sair do **HC** e ligar diretamente os **MUTOAs**, uma vez que, estes precisam de um **alto nível de tráfego de dados** até porque estes vão apresentar 6 outlets (usando, por exemplo, o **Mutoa**: *"MINI -C OM ® MuTOA 6 Port Outlet Box"*)


* Utilizei cabos de **fibra ótica multivalor** até ao **HC**, uma vez que o comprimento dos cabos não justifica a utilização de cabos de **fibra ótica monomodo** (o que seria melhor caso os cabos que estariam a ser utilizados tivessem mais que 1KM, e uma vez que, os mesmos são imunes à **dispersão** devido ao raio do seu núcleo ser tão pequeno) e, portanto, permite **taxas de dados altas** até porque o **HC** é o fim do **Backbone**, ou seja é ele que fica responsável pelo piso.
  A partir do **HC** utilizei apenas cabos de cobre - **CAT6** e cabos de cobre - **CAT7** na distribuição do piso. Foram utilizados, respetivamente, cabos **CAT7** entre o **HC** e os 2 **APs** e os 3 **MUTOAs** que se encontram neste piso e também entre a ligação do **HC** e os 4 **CPs**, e cabos **CAT6** entre os **CPs** e os outlets.

  
* Achei pertinente utilizar cabos **CAT7** entre o **HC** e os **AP** representados no sketch, pois o mesmo permite **alto nível de tráfego de dados**;


* Devido às paredes de betão armado que existem no piso, temos de ter em consideração o fator que o raio de alcance de cada **AP** é reduzido por volta de 10-20 metros, o que vai fazer com que seja necessário **2 APs** no mesmo piso para que fique completamente coberto por wireless;


* Para alcançar tanto os **outlets** como os **MUTOAs** que se encontram no meio da sala, é utilizado calha para esconder e organizar os cabos, sendo esta colada ao chão (e caso fosse necessário poderia existir tomadas elétricas nesta mesma calha);


* Os **APs** deste andar foram distribuídos do modo que conseguissem cobrir o máximo possível com wireless o piso 0 e possivelmente entrada e arredores.
  No sketch do piso 1 vai ser possível que os **APs** se encontram colocados respetivamente aos do piso 0 de uma forma simétrica possibilitando assim o máximo de cobertura possível com apenas 4 **APs** no total (no edifício todo).


* Para alimentação dos **AP** o cabo **CAT7** irá utilizar a tecnologia **POE** para alimentar de energia elétrica os equipamentos. Irão ser utilizados **Power Injectors** para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do **HC** para assim alimentar a ligação.


* Todos os **patch cords** vão seguir a regra que tem de ter um comprimento entre **0.5 - 5 metros**.


* Na maioria das salas, tal como mencionado numa nota debaixo do sketch, vao existir cabos a passar por calhas que se encontram no teto falso (teto falso que cobre por completo o andar todo).


## **Cálculos e finais observações**

* Para determinar o número de outlets necessários para cada divisão, baseei-me na seguinte regra: **"Os padrões de cabeamento estruturado especificam um mínimo de duas saídas por área de trabalho, também duas saídas para cada 10 metros quadrados de área. Portanto, para uma área de trabalho acima de 10 m^2, quatro saídas devem estar disponíveis."**


* Na distribuição dos outlets de forma estruturada segui a seguinte regra :**"A localização das tomadas dentro da área de trabalho deve ser tal que o equipamento do usuário final
  está ao alcance usando os patch cords de até cinco metros de comprimento e também fornecem
  flexibilidade para que os usuários possam mover seus equipamentos. Onde quer que o usuário
  equipamento é, deve haver sempre uma tomada a menos de três metros de distância".**
  
  
* Em relação à redundância de cabos do backbone segui e implementei esta regra :**"Cada conexão de backbone deve ser um conjunto de vários cabos paralelos. Este conjunto
  de vários cabos pode ser usado de várias maneiras:
  Use um único, se algum dia falhar, o operador pode alternar para outro
  Isso é chamado de failover (neste caso, failover manual).
  O mesmo de antes, mas automático. Usando os protocolos apropriados, a camada 2
  (comutação) e os dispositivos de camada 3 (roteamento) detectam se um cabo está falhando e
  alternar automaticamente para outro.
  O mesmo que antes, mas todos os cabos alternativos são usados ao mesmo tempo para
  transmitir dados com balanceamento de carga. Isso não é mais chamado de failover, mas se um
  cabo falhar, ele não será mais usado."** Ou mesmo, na PL1 existe esta informação também : **"Conexões redundantes de cabos de backbone são desejáveis, elas fornecem tolerância a falhas (failover) e também podem
  ser usado para aumentar a largura de banda (balanceamento de carga de rede). No que diz respeito a cabos redundantes, estes
  recursos podem ser habilitados posteriormente nos switches da camada dois (Spanning Tree Protocol e Link Aggregation
  Control Protocol) ou nos roteadores da camada três (Dynamic Routing Protocols)."**
  

* Em relação aos **TEs** segui tanto esta regra: **"each cross-connect will have at least one
telecommunication enclosure, 19” rack enclosures vertical size is measured in
U rack units (1.75’’/44.45 mm). Typical CAT7 24 ports patch panels have 1U
size. Defining the enclosure size reflects what we already know: the patch
panels that will be fitted there, but that’s not enough, active equipment will
also be placed there."**, como também : **"One thing to bear in mind is that these enclosures will house not
only the wiring termination hardware but also active equipment
that is not part of the cabling system itself like switches, routers,
servers, UPS (Uninterruptible Power Supply), etc.
The exact size of telecommunications enclosures cannot be derived from the
cabling system only, it must also take in account space for other hardware.
Also, an up to 50% oversizing is wise to accommodate future upgrades."**
  


* Para além dos *.png* disponibilizados dos sketches do piso 0 e do piso 1, também foi disponibilizado o *.svg*, mas o mesmo encontra-se com problemas de formatação quando foi exportado, por isso optamos por utilizar os *.png* na apresentação do ficheiro markdown.