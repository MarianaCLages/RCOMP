# RCOMP 2021-2022 Project - Sprint 1 - Member 1200920 folder

# Backbone

A estrutura de cablagem preposta para o exterior está representada na figura abaixo:

![EstruturaExterior](/doc\sprint1\1200920\Exterior.svg)

**Legenda: Figura representativa das diferentes medidas necessárias do campus**

## Localização dos cross-connects

**Main cross-connect (MC), Distributor C (DC) or Campus Distributor (CD)**: encontrar-se-á no edifício 1 como é pedido no enunciado.

**Intermediate cross-connect (IC), Distributor B (DB) or Building Distributor (BD)**: Será colocado 1 no primeiro piso de cada edifício, ligado ao MC que se encontra no Edifício 1.

**Horizontal cross-connect (HC), Distributor A (DA) or Floor Distributor (FD)**: Será colocado 1 em cada andar de cada edifício, ligados ao IC do respetivo edifício, que se encontra no piso térreo.

## Tipo de cabos utilizados

Como as distâncias entre os diferentes edifícios são consideravelmente elevadas e queremos tirar partido máximo da velocidade de ligação á rede providenciada pelo ISP (Internet Service Provider), serão adotados cabos do tipo fibra ótica (especificados abaixo) entre o MC, que se encontra no edifício 1, e os IC´s dos edifícios. Dentro dos edifícios, devido à baixa distancia entre dispositivos será usado cabo de cobre CAT7.

<p> Paragrafo sobre a fibra que usamos </p>
De modo a prevenir eventuais falhas de cabos será adotada redundância de cabos entre MC e IC.

# Edifício 1

## **_Floor 0_**

![Floor0_Building1](/doc\sprint1\1200920\1.0.png)

#

### _Notas:_

- **Nota 1**: Os cabos representados perto e paralelos à parede (ou dentro da parede) representam cabos na parede cobertos por calhas, assim como as tomadas junto à parede significam que elas estão colocadas na mesma.

- **Nota 2:** Como é possível observar no sketch, para alcançar as tomadas que se encontram no meio da sala é utilizado calha para cobrir os mesmo (tanto para o mutoa como para tomadas).

#

### _Informações:_

| Sala             | Área      | Outlets    | CP                                    |
| :--------------- | :-------- | :--------- | :------------------------------------ |
| 1.0.1            | 19.04 m^2 | 4 Outlets  | 0                                     |
| 1.0.2 Datacenter | 31.28 m^2 | 6 Outlets  | 1 (Switch e patch panel de 42 portas) |
| 1.0.3            | 27.2 m^2  | 6 Outlets  | 0                                     |
| 1.0.4            | 42.84 m^2 | 10 Outlets | 1 (Switch e patch panel de 24 portas) |
| 1.0.5            | 13.8 m^2  | 4 Outlets  | 0                                     |
| 1.0.6            | 13.8 m^2  | 4 Outlets  | 1 (Switch e patch panel de 12 portas) |
| 1.0.7            | 13.8 m^2  | 4 Outlets  | 0                                     |
| 1.0.8            | 23 m^2    | 6 Outlets  | 1 (Switch e patch panel de 16 portas) |
| 1.0.9            | 26.22 m^2 | 6 Outlets  | 0                                     |
| 1.0.10           | 41.61 m^2 | 10 Outlets | 1 (Switch e patch panel de 16 portas) |

### Inventário do Piso 0

- x metros de cabo fibra multi-modo
- x metros de cabo cat7
- x metros de cabo cat6
- 1 Switch de 42 portas
- 1 Switch de 24 portas
- 2 Switch de 16 portas
- 1 Switch de 12 portas
- 1 patch panel de 42 portas
- 1 patch panel de 24 portas
- 2 patch panel de 16 portas
- 1 patch panel de 12 portas
- 1 AP
- 1 Power Injectors
- 60 Outlets
- 1 MUTOA
- 1 MC
- 1 IC
- 4 19'' Telecommunications Enclosures
- 1 grande (??) Telecommunications Enclosures

### Observações de Implementação

- Devido á natureza da sala 1.0.2 (Datacenter) foram escolhidos um switch e um patch panel com imensas portas disponíveis.

- Foi usado 1 **MUTOA** neste andar, precisamente, na sala 1.0.4, uma vez que existe **uma área ampla no meio da sala** e assumindo que esta sala terá uma grande densidade de utilizadores a opção é justificada. Irá ser passada uma calha pelo chão até ao local em que pretende instalar o equipamento, não irá causar transtorno aos utilizadores do espaço, uma vez que as calhas são calhas de baixo relevo.

- Entre os **HC** e os **CP** e os **AP** será usado cabo **CAT7**, pois o mesmo permite **alto nível de tráfego de dados**.

- Para alimentação dos **AP** o cabo **CAT7** irá utilizar a tecnologia **POE** para alimentar de energia elétrica os equipamentos. Irão ser utilizados **Power Injectors** para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do **HC** para assim alimentar a ligação.

- Devido às paredes de betão armado que existem no piso, temos de ter em consideração o fator que o raio de alcance de cada **AP** é reduzido por volta de 10 metros, o que vai fazer com que seja necessário **1 APs** no mesmo piso para que fique completamente coberto por wireless.

- O cabo irá ser correr entre as diversas salas e os diversos dispositivos através da calha subterrânea já implementada no edifício.

# **_Floor 1_**

![Floor1_Building4](/doc\sprint1\1200920\1.1.png)

#

### _Informações:_

| Sala   | Área      | Outlets    | CP                                    |
| :----- | :-------- | :--------- | :------------------------------------ |
| 1.1.1  | 21.76 m^2 | 4 Outlets  | 1 (Switch e patch panel de 16 portas) |
| 1.1.2  | 51 m^2    | 10 Outlets | 0                                     |
| 1.1.3  | 55.76 m^2 | 12 Outlets | 1 (Switch e patch panel de 24 portas) |
| 1.1.4  | 42.84 m^2 | 10 Outlets | 0                                     |
| 1.1.5  | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.6  | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.7  | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.8  | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.9  | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.10 | 14.5 m^2  | 2 Outlets  | 1 (Switch e patch panel de 12 portas) |
| 1.1.11 | 14.5 m^2  | 2 Outlets  | 1 (Switch e patch panel de 12 portas) |
| 1.1.12 | 14.5 m^2  | 2 Outlets  | 0                                     |
| 1.1.13 | 14.5 m^2  | 2 Outlets  | 1 (Switch e patch panel de 8 portas)  |
| 1.1.14 | 40.47 m^2 | 8 Outlets  | 1 (Switch e patch panel de 12 portas) |

### Inventário do Piso 0

- x metros de cabo fibra multi-modo
- x metros de cabo cat7
- x metros de cabo cat6
- 1 Switch de 24 portas
- 1 Switch de 16 portas
- 3 Switch de 12 portas
- 1 Switch de 8 portas
- 1 Patch Panel de 24 portas
- 1 Patch Panel de 16 portas
- 3 Patch Panel de 12 portas
- 1 Patch Panel de 8 portas
- 2 AP
- 2 Power Injectors
- 53 Outlets
- 1 MUTOA
- 1 HC
- 6 19'' Telecommunications Enclosures

### Observações de Implementação

- Devido á pequena dimensão das salas 1.1.5 a 1.1.13 assumimos que estas salas vão ter uma densidade pequena de utilizadores, idealmente apenas um ou dois utilizadores, assim decidi que apenas iriam ser colocados 2 outlets em cada um destas salas.

- Devido ao dispormos de um teto falso iremos usar este teto falso para passar os cabos entre salas e dispositivos, fazendo-os assim sair do teto em calhas pelas paredes para ligar quer aos **outlets** quer aos **CP**. Dentro do teto falso irão ser usadas calhas para guiar melhor os cabos e assim manter a organização.

- Foi usado 1 **MUTOA** neste andar, precisamente, na sala 1.1.3, uma vez que existe **uma área ampla no meio da sala** e assumindo que esta sala terá uma grande densidade de utilizadores a opção é justificada. Irá ser passada uma calha pelo chão até ao local em que pretende instalar o equipamento, não irá causar transtorno aos utilizadores do espaço, uma vez que as calhas são calhas de baixo relevo;

- Entre os **HC** e os **CP** e os **AP** será usado cabo **CAT7**, pois o mesmo permite **alto nível de tráfego de dados**;

- Para alimentação dos **AP** o cabo **CAT7** irá utilizar a tecnologia **POE** para alimentar de energia elétrica os equipamentos. Irão ser utilizados **Power Injectors** para permitir ao cabo transportar energia elétrica. Estes dispositivos irão ser colocados na saida do **HC** para assim alimentar a ligação.

- Devido às paredes de betão armado que existem no piso, temos de ter em consideração o fator que o raio de alcance de cada **AP** é reduzido por volta de 10 metros, o que vai fazer com que seja necessário **2 APs** no mesmo piso para que fique completamente coberto por wireless;
