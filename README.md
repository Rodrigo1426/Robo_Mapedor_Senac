# Robo_Mapedor_Senac
Integrantes do grupo:
Rodrigo Mulinário Ramos: A

Thales Durães de Lima: PA

Victor Alves Barbosa: PA

Wagner Bento Santo: PA

##### Este robô utiliza um módulo de Arduino MCU Node ESP-8266 que se comunica com um telefone celular por wifi. O telefone executa um aplicativo criado na engine Unity 3D e é possível fazer 3 coisas:

1.)	A primeira cena permite que você dirija o robô com um smartphone acoplado ao chassi, se comunicando com o computador. Você pode usar as setas do teclado para dirigir em qualquer direção e o feed de vídeo permite que você continue dirigindo mesmo quando o robô está fora de vista.

2.)	A segunda cena permite que robô rastreie qualquer coisa que você coloque na frente dele. Você pode clicar na tela do smartphone para  que o rastreador foque em um objeto, e em seguida o robô seguirá o mesmo. (Ainda tem teste)

3.)	A terceira cena permite que você controle o robô com seu computador usando as teclas de seta. O aplicativo usa um SDK de realidade aumentada para encontrar as paredes e o chão pelo aplicativo no smartphone, envia as informações para o Unity, e fornece uma representação digital do seu ambiente.
(Somente Iphone)
  
![Alt Text]  (https://github.com/Rodrigo1426/Robo_Mapedor_Senac/blob/master/Mapping_Room_bb.png)
  
## Peças
 
1.)	ESP-8266 Node MCU;

2.)	L298N Motor Driver;

3.) Fios de Arduino;

4.)	2 chassis de robô, 4 rodas, dois compartimentos de 4 pilhas

## Passo 1: Fazendo as conexões!

Para conectar os motores e a placa Arduino, usaremos uma ponte H dupla L298N, esse módulo permite girar os motores em diferentes direções.
Esse módulo tem um “input” de até 12 volts e tem um regulador de tensão que gera um “output” de 5V.
Conecte tudo de acordo com o diagrama abaixo.
 
## Passo 2: montado o robô!

Utilize 2 chassis para montar seu robô. Entre os chassis fixe os módulos L298N e o ESP12 8266 com fita dupla face.
Coloque os 2 compartilhamentos de pilha em cada lado do chassi, também fixos com fita dupla face.
Coloque os motores e as rodas conforme o manual.
Fixe seu celular na parte de cima do 2° chassi com um enforca gato, ou com um tripé

## Passo 3: copie e cole o código AR_Arduino (encontrado no repositório)!

## Passo 4: conecte todos os dispositivos à sua rede.

Toda a comunicação é feita via WiFi, portanto, certifique-se de que seu smartphone e computador estejam conectados à mesma rede local.
Com o ESP12 8266 conectado via USB, abra o monitor serial no Arduino IDE para 115200 BAUD.
Pressione reset no ESP12 e espere a placa se conectar à sua rede. Ele gravará seu endereço IP.
Copie esse IP e cole em um bloco de notas pois precisaremos inserir esse IP no Unity.
Vá esse link no Github, baixe e abra este projeto no Unity:
https://github.com/MatthewHallberg/AR_Robot
