# Projeto de Organização de Computadores: Entrada/Saída (I/O)

## Descrição
Este projeto aborda os conceitos de Entrada/Saída (I/O) no contexto da Organização de Computadores. 
Focamos no desenvolvimento e simulação de um sistema que demonstra a integração entre sensores e dispositivos de saída, mostrando como a comunicação entre hardware e software é essencial para sistemas computacionais modernos.

<details>
  <summary><strong>Objetivos</strong></summary>
  <ul>
    <li>Compreender o funcionamento dos dispositivos de Entrada e Saída (I/O).</li>
    <li>Desenvolver um protótipo utilizando sensores (entrada) e displays/LEDs (saída).</li>
    <li>Simular a comunicação entre os componentes para reforçar conceitos teóricos da disciplina.</li>
  </ul>
</details>

<details>
  <summary><strong>Requisitos</strong></summary>
  <ul>
    <li>Conta no Tinkercad para simulação de circuitos.</li>
    <li>Arduino IDE para programação do microcontrolador.</li>
    <li>Componentes: LEDs, resistores, sensores (PIR, temperatura), display LCD.</li>
    <li>Bibliotecas Arduino:
      <ul>
        <li><code>Adafruit_LiquidCrystal</code></li>
        <li><code>Wire.h</code></li>
      </ul>
    </li>
  </ul>
</details>

<details>
  <summary><strong>Como Executar</strong></summary>
  <ol>
    <li>Acesse o Tinkercad e faça login com sua conta.</li>
    <li>Importe o arquivo do circuito disponível no <a href="https://www.tinkercad.com/">link do Tinkercad</a>.</li>
    <li>No Tinkercad, carregue o código fornecido em <code>codigo.ino</code> e execute a simulação.</li>
    <li>No Arduino IDE, instale as bibliotecas necessárias (<code>Adafruit_LiquidCrystal</code>, <code>Wire</code>).</li>
    <li>Conecte os componentes conforme o esquema abaixo:</li>
  </ol>
  <img src="imagens/esquema_ligacao.png" alt="Esquema de ligação">
</details>

<details>
  <summary><strong>Demonstração</strong></summary>
  <h4>Esquema de Montagem</h4>
  <img src="imagens/esquema.png" alt="Esquema">

  <h4>Resultado da Simulação</h4>
  O display LCD exibirá mensagens de acordo com a leitura dos sensores. Os LEDs acenderão em resposta a determinadas entradas, demonstrando o conceito de I/O em sistemas de computadores.
</details>

<details>
  <summary><strong>Explicação Técnica</strong></summary>
  <p>O sistema utiliza sensores (PIR e temperatura) como dispositivos de entrada. O Arduino processa os sinais dos sensores e envia comandos para os dispositivos de saída (display LCD, LEDs). O código é responsável por interpretar os dados dos sensores e atualizar as saídas em tempo real.</p>

  <h4>Principais Trechos do Código</h4>
  ```cpp
  Wire.requestFrom(8, 1);  // Solicita dados do sensor
  if (Wire.available()) {
      int state = Wire.read();
      lcd1.print("Movimento detectado");
  }
