## 🤖 League of Robots 🤖 - Material para a competição
[voltar](../README.md)

### Api básica

1. [Movimentação - Robot](API.md#1-movimentação---robot)
1. [Movimentação - AdvancedRobot](API.md#2-movimentação---advancedrobot)
1. [Movimentação - AdvancedRadiansRobot](API.md#3-movimentação---advancedradiansrobot)
1. [Tiro - Robot](API.md#4-tiro---robot)
1. [Tiro - AdvancedRobot](API.md#5-tiro---advancedrobot)
1. [Envia Dados Para O Robô](API.md#6-envia-dados-Para-o-robô)
1. [Retorna Dados do Rôbo](API.md#7-retorna-dados-do-robô---robot)
1. [Retorna Dados do Robô - AdvancedRadiansRobot](API.md#8-retorna-dados-do-robô---AdvancedRadiansRobot)
1. [Retorna Dados da Batalha](API.md#9-retorna-dados-da-batalha)
1. [Outros](API.md#10-outros)

#### Links externos

1. [Robocode API (Java)](https://robocode.sourceforge.io/docs/robocode)
1. [Robocode .NET API](https://robocode.sourceforge.io/docs/robocode.dotnet/Index.html)
1. [Robocode .NET Control API](https://robocode.sourceforge.io/docs/robocode.dotnet.control/Index.html)

#### 1. Movimentação - Robot
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comando|Parâmetro|Descrição|
|---|--- |--- |
|ahead( double )|a distância que o robô deverá percorrer.|Movimenta o robô para frente, uma distância x dada por parâmentro. Se o robô bater em outro, ou na parede antes de completar a distancia desejada o método é interrompido.|
|back( double )|a distância que o robô deverá percorrer.|Semelhante ao método anterior, a única diferença é que o robô move para traz.|
|turnRight( double )|o ângulo em graus que o robô deverá girar.|Gira o robô para a direita (sentido horário).|
|turnLeft( double )|o ângulo em graus que o robô deverá girar.|Gira o robô para a esquerda (sentido anti-horário).|
|turnGunRigth( double )|o ângulo em graus que o canhão deverá girar|Gira o canhão para a direita.|
|turnGunLeft( double )|o ângulo em graus que o canhão deverá girar|Gira o canhão para a esquerda.|
|turnRadarRigth( double )|o ângulo em graus que o radar deverá girar|Gira o radar para a direita.|
|turnRadarLeft( double )|o ângulo em graus que o radar deverá girar|Gira o radar para a esquerda.|

#### 2. Movimentação - AdvancedRobot
[Topo](API.md#-league-of-robots----material-para-a-competição)

Os comandos da classe AdvancedRobot que começam com "set" eles funcionam como os herdados da classe Robot. A diferença é que enquanto o método está sendo executado ele continua executando as linhas de comando abaixo. Com isso é possível misturar movimentos. Por exemplo, se tiver `turnRight(90);` o robô irá andar para frente e depois que tiver terminado de percorrer a distância 100, ele girará 90º. Mas se tiver `setTurnRight(90);` o robô andará para frente e girará 90º ao mesmo tempo, fazendo uma curva.

|Comando|Parâmetro|Descrição|
|--- |--- |--- |
|setAhead( double )|a distância que o robô deverá percorrer.|Herdado do método ahead.|
|setBack( double )|a distância que o robô deverá percorrer.|Herdado do método back.|
|setTurnRight( double )|o ângulo em graus que o robô deverá girar.|Herdado do método turnRight.|
|setTurnLeft( double )|o ângulo em graus que o robô deverá girar.|Herdado do método turnLetf.|
|setTurnGunRigth( double )|o ângulo em graus que o canhão deverá girar|Herdado do método turnGunRigth.|
|setTurnGunLeft( double )|o ângulo em graus que o canhão deverá girar|Herdado do método turnGunLeft.|
|setTurnRadarRigth( double )|o ângulo em graus que o radar deverá girar|Herdado do método turnRadarRigth.|
|setTurnRadarLeft( double )|o ângulo em graus que o radar deverá girar|Herdado do método turnRadarLeft.|


#### 3. Movimentação - AdvancedRadiansRobot
[Topo](API.md#-league-of-robots----material-para-a-competição)

Esses métodos "Radians" são usados quando vai se trabalhar com PI, seno, cosseno, tangente.  
Os métodos que começam com "set" são como aqueles visto acima, que continuam lendo as linhas de comando abaixo, misturando movimentos.

|Comando|Parâmetro|Descrição|
|--- |--- |--- |
|turnRightRadians( double )|o ângulo em radianos|Gira o robô para a direita.|
|turnRightRadians( double )|o ângulo em radianos|Gira o robô para a esquerda.|
|turnGunRightRadians( double )|o ângulo em radianos|Gira o canhão para a direita.|
|turnGunLeftRadians( double )|o ângulo em radianos|Gira o canhão para a esquerda.|
|turnRadarRigthRadians( double )|o ângulo em radianos|Gira o radar para a direita.|
|turnRadarLeftRadians( double )|o ângulo em radianos|Gira o radar para a esquerda.|
|setTurnRightRadians( double )|o ângulo em radianos|Herdado do método turnRightRadians.|
|setTurnLeftRadians( double )|o ângulo em radianos|Herdado do método turnLeftRadians.|
|setTurnGunRightRadians( double )|o ângulo em radianos|Herdado do método turnGunRightRadians.|
|setTurnGunLeftRadians( double )|o ângulo em radianos|Herdado do método turnGunLeftRadians.|
|setTurnRadarRigthRadians( double )|o ângulo em radianos|Herdado do método turnRadarRightRadians.|
|setTurnRadarLeftRadians( double )|o ângulo em radianos|Herdado do método turnRadarLeftRadians.|

#### 4. Tiro - Robot
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comando|Parâmetro|Descrição|
|--- |--- |--- |
|fire( double )|a força do tiro, e subtraido da energia de seu robô.|Atira imediatamente na força mandada por parâmetro,de 0.1 até 3. Se mandar um tiro maior que 3 ele considera força 3.|
|fireBullet( double )|a força do tiro, e subtraido da energia de seu robô.|A diferença do método anterior é que ele é uma função e retorna um valor do tipo Bullet, além disso, manda outro tiro em seguida, este com mais velocidade, se o primeiro tiro tiver boas possibilidades da acertar.|


#### 5. Tiro - AdvancedRobot
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comandos|Parâmetro|Descrição|
|--- |--- |--- |
|setFire( double )|a força do tiro, e subtraido da energia de seu robô.|Herdado do método fire.|
|setFireBullet( double )|a força do tiro, e subtraido da energia de seu robô.|Herdado do método fireBullet.|


#### 6. Envia Dados Para O Robô
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comando|Parâmetro|Descrição|
|--- |--- |--- |
|setAdjustGunForRobotTurn( boolean )|||
|setAdjustRadarForGunTurn( boolean )|||
|setColors( Color, Color, Color )|a cor do robô, a cor do canhão, a cor do radar, nesta ordem.|Atribui as cores do robô.|


#### 7. Retorna Dados do Rôbo
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comando|Tipo do Retorno|Descrição do Retorno|
|--- |--- |--- |
|getName()|String|Retorna o nome do robô.|
|getEnergy()|double|Retorna a energia corrente do robô.|
|getX()|double|A posição X(eixo horizontal) do robô na arena de batalha. Quando 0(zero) ele estará encostado no lado esquerdo.|
|getY()|double|A posição Y(eixo vertical) do robô na arena de batalha. Quando 0(zero) ele estará encostado na parte de baixo.|
|getWidth()|double|Retorna a largura do robô.|
|getHeight()|double|Retorna a altura do robô.|
|getHeading()|double|Retorna o ângulo em graus ( de 0 até 360 ) que o robô está virado. Se retornar 0(zero) ele está virado para a esquerda, se retornar 90 ele está voltado para cima.|
|getGunHeading()|double|Retorna o ângulo em graus que o canhão está virado. Como no método anterior.|
|getRadarHeading()|double|Retorna o ângulo em graus que o radar está virado.|
|getGunCoolingRate()|double||
|getGunHeat()|double|Retorna quanto o canhão está virando no momento corrente.|
|getVelocity()|double|Retorna a velocidade do robô.|


#### 8. Retorna Dados do Robô - AdvancedRadiansRobot
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comandos|Tipo do Retorno|Retorno|
|--- |--- |--- |
|getHeadingRadians()|double|Retorna a direção que o robô está voltado, em radianos (de 0 até 2*PI).|
|getGunHeadingRadians()|double|Retorna o ângulo em radianos do canhão está apontado em relação a tela|
|getRadarHeadingRadians()|double|Retorna o ângulo em radianos do radar está voltado em relação a tela|
|getTurnRemainingRadians()|double||
|getGunTurnRemainingRadians()|double||
|getRadarTurnRemainingRadians()|double||


#### 9. Retorna Dados da Batalha
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comandos|Tipo do Retorno|Retorno|
|--- |--- |--- |
|getOthers()|int|Retorna o total de oponentes ainda vivos no round.|
|getBattleFieldHeight()|double|Retorna a altura da arena de batalha.|
|getBattleFieldWidth()|double|Retorna a largura da arena de batalha.|
|getNumRounds()|int|Retorna o total de rounds da batalha.|
|getRoundNum()|int|Retorna o número do round corrente.|
|getTime()|long|Retorna o tempo do round. Quando inicia outro round o tempo volta a 0(zero). O é tempo equivale ao número de quabgazul.jpgdros mostrados.|


#### 10. Outros
[Topo](API.md#-league-of-robots----material-para-a-competição)

|Comando|Parâmetro|Descrição|
|--- |--- |--- |
|doNothing()|nenhum parâmetro||
|scan()|nenhum parâmetro||
|stop()|nenhum parâmetro||
|stop( boolean )|||
|resume()|nenhum parâmetro||
|setResume()|nenhum parâmetro||
|setStop()|nenhum parâmetro||
|setStop( boolean )|||
|finalize()|nenhum parâmetro||


##### [Topo](API.md#-league-of-robots----material-para-a-competição) | [Página principal](../README.md)