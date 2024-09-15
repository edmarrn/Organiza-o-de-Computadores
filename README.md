# Projeto de Organização de Computadores: Entrada/Saída (I/O) - IFRN 2024.1

![Descrição do Projeto](https://github.com/user-attachments/assets/835400cb-497f-4618-891a-5883e915fcac)

<details>
<summary>Descrição</summary>
Este projeto aborda os conceitos de Entrada/Saída (I/O) no contexto da Organização de Computadores. Focamos no desenvolvimento e simulação de um sistema que demonstra a integração entre sensores e dispositivos de saída, mostrando como a comunicação entre hardware e software é essencial para sistemas computacionais modernos.
</details>

<details>
<summary>Objetivos</summary>
- Compreender o funcionamento dos dispositivos de Entrada e Saída (I/O).<br>
- Desenvolver um protótipo utilizando sensores (entrada) e displays/LEDs (saída).<br>
- Simular a comunicação entre os componentes para reforçar conceitos teóricos da disciplina.
</details>

<details>
<summary>Requisitos</summary>
- Conta no Tinkercad para simulação de circuitos.<br>
- Arduino IDE para programação do microcontrolador.<br>
- Componentes: LEDs, resistores, sensores (PIR, temperatura), display LCD.<br>
- Bibliotecas Arduino:<br>
    - `Adafruit_LiquidCrystal`
    - `Wire.h`
</details>

<details>
<summary>Como Executar</summary>
1. Acesse o Tinkercad e faça login com sua conta.<br>
2. Importe o arquivo do circuito disponível no [link do Tinkercad](https://www.tinkercad.com/).<br>
3. No Tinkercad, carregue o código fornecido em `codigo.ino` e execute a simulação.<br>
4. No Arduino IDE, instale as bibliotecas necessárias (`Adafruit_LiquidCrystal`, `Wire`).<br>
5. Conecte os componentes conforme o esquema abaixo:<br>

  ![image](https://github.com/user-attachments/assets/fddd0327-de2e-4ca5-91bd-9cf9e4a90711) <br><br>
  
  ![image](https://github.com/user-attachments/assets/50545d72-1611-4233-b920-5a56a1a77a0c)

  

</details>

<details>
<summary>Demonstração</summary>
  Abaixo estão a demonstração e os resultados do desenvolvimento do projeto, ilustrados pelas imagens:

  Figura 1:
  ![image](https://github.com/user-attachments/assets/62bdebcf-fced-470c-a18a-6e1a26677278) <br>

  Figura 2:
  ![image](https://github.com/user-attachments/assets/659c30ae-685e-42c0-a107-cd3e8ddeda77) <br>

  Figura 3:
  ![image](https://github.com/user-attachments/assets/5d7dd9e4-a6fa-4c6a-b219-6a8e6b13e7db) <br>


</details>
<details>
<summary>Explicação Técnica</summary>
O sistema desenvolvido utiliza sensores PIR (Passive Infrared) como dispositivos de entrada para monitorar e detectar movimentos. O sensor PIR detecta a presença de movimento. Esses sensores estão conectados ao Arduino, que atua como a unidade central de processamento.

O Arduino recebe e processa os sinais enviados pelos sensores, analisando os dados em tempo real. Com base nas condições pré-programadas no código, o Arduino então aciona os dispositivos de saída: um display LCD e LEDs. O display LCD exibe mensagens que refletem o estado atual dos sensores, como "Movimento Detectado". Simultaneamente, os LEDs acendem ou apagam em resposta aos eventos capturados pelos sensores, proporcionando um feedback visual instantâneo.

O código implementado é fundamental para a operação do sistema. Ele realiza a leitura contínua dos sensores, interpreta os dados coletados e toma decisões para atualizar os dispositivos de saída de forma eficiente. Esse processo garante a comunicação sincronizada entre entrada e saída, simulando como os sistemas embarcados lidam com múltiplas fontes de dados e interações em um ambiente real.
</details>
<details>
<summary>Principais Trechos do Código</summary>
Wire.requestFrom(8, 1);  // Solicita dados do sensor
if (Wire.available()) {
    int state = Wire.read();
    lcd1.print("Movimento detectado");
}
</details>
