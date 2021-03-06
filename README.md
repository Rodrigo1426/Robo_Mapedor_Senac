# Robo Mapeador Senac Tatuapé
Integrantes do grupo:
Rodrigo Mulinário Ramos: A

Thales Durães de Lima: PA

Victor Alves Barbosa: PA

Wagner Bento Santo: PA

### Este robô utiliza um módulo de Arduino MCU Node ESP-8266 que se comunica com um telefone celular por wifi. O telefone executa um aplicativo criado na engine Unity 3D e é possível fazer 3 coisas:

1.)	A primeira cena permite que você dirija o robô com um smartphone acoplado ao chassi, se comunicando com o computador. Você pode usar as setas do teclado para dirigir em qualquer direção e o feed de vídeo permite que você continue dirigindo mesmo quando o robô está fora de vista.

2.)	A segunda cena permite que robô rastreie qualquer coisa que você coloque na frente dele. Você pode clicar na tela do smartphone para  que o rastreador foque em um objeto, e em seguida o robô seguirá o mesmo. (Ainda tem teste)

3.)	A terceira cena permite que você controle o robô com seu computador usando as teclas de seta. O aplicativo usa um SDK de realidade aumentada para encontrar as paredes e o chão pelo aplicativo no smartphone, envia as informações para o Unity, e fornece uma representação digital do seu ambiente.
(Somente Iphone)
  
  
## Peças
 
1.)	ESP-8266 Node MCU;

![esp](https://user-images.githubusercontent.com/43183325/45571726-91986680-b83d-11e8-8a9e-ec4e393f15b1.png)

2.)	L298N Motor Driver;

![l298](https://user-images.githubusercontent.com/43183325/45571742-9eb55580-b83d-11e8-8122-7eb2b8e6ca55.png)

3.) Fios de Arduino;

![fio](https://user-images.githubusercontent.com/43183325/45571730-9826de00-b83d-11e8-94e4-933b742c627c.png)

4.)	2 chassis de robô, 4 rodas, dois compartimentos de 4 pilhas

![chassi](https://user-images.githubusercontent.com/43183325/45571760-ab39ae00-b83d-11e8-8117-15a050947fc8.png)


## Passo 1: Fazendo as conexões!

Para conectar os motores e a placa Arduino, usaremos uma ponte H dupla L298N, esse módulo permite girar os motores em diferentes direções.
Esse módulo tem um “input” de até 12 volts e tem um regulador de tensão que gera um “output” de 5V.
Conecte tudo de acordo com o diagrama abaixo.

![mapping_room_bb](https://user-images.githubusercontent.com/43183325/45571590-159e1e80-b83d-11e8-8788-20402695dafe.png)
 
## Passo 2: montado o robô!

Utilize 2 chassis para montar seu robô. Entre os chassis fixe os módulos L298N e o ESP12 8266 com fita dupla face.
Coloque os 2 compartilhamentos de pilha em cada lado do chassi, também fixos com fita dupla face.
Coloque os motores e as rodas conforme o manual.
Fixe seu celular na parte de cima do 2° chassi com um enforca gato, ou com um tripé

 ![robo](https://user-images.githubusercontent.com/43183325/45571751-a412a000-b83d-11e8-82ce-0ccd0aca1d6a.png)

## Passo 3: copie e cole o código AR_Arduino 
https://github.com/Rodrigo1426/Robo_Mapedor_Senac/blob/master/AR_Arduino.ino

## Passo 4: conecte todos os dispositivos à sua rede.

Toda a comunicação é feita via WiFi, portanto, certifique-se de que seu smartphone e computador estejam conectados à mesma rede local.
Com o ESP12 8266 conectado via USB, abra o monitor serial no Arduino IDE para 115200 BAUD.
Pressione reset no ESP12 e espere a placa se conectar à sua rede. Ele gravará seu endereço IP.
Copie esse IP e cole em um bloco de notas pois precisaremos inserir esse IP no Unity.
Vá esse link no Github, baixe e abra este projeto no Unity:
https://github.com/MatthewHallberg/AR_Robot

#### Agradecimentos ao Matthew Hallberg por disponibilizar o código fonte do projeto.
https://github.com/MatthewHallberg
