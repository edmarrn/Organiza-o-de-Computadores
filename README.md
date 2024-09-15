# Projeto de Organização de Computadores: Entrada/Saída (I/O) - IFRN 2024.1

## Descrição
Este projeto aborda os conceitos de Entrada/Saída (I/O) no contexto da Organização de Computadores. Focamos no desenvolvimento e simulação de um sistema que demonstra a integração entre sensores e dispositivos de saída, mostrando como a comunicação entre hardware e software é essencial para sistemas computacionais modernos.

![image](https://github.com/user-attachments/assets/835400cb-497f-4618-891a-5883e915fcac)

<details>
  <summary>Objetivos</summary>
  <ul>
    <li>Compreender o funcionamento dos dispositivos de Entrada e Saída (I/O).</li>
    <li>Desenvolver um protótipo utilizando sensores (entrada) e displays/LEDs (saída).</li>
    <li>Simular a comunicação entre os componentes para reforçar conceitos teóricos da disciplina.</li>
  </ul>
</details>

<details>
  <summary>Requisitos</summary>
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
  <summary>Como Executar</summary>
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
  <summary>Demonstração</summary>

  <h4>Esquema de Montagem</h4>
  <img src="https://github.com/user-attachments/assets/ed166378-be6e-4786-8df0-14f99834c849/raw" alt="Esquema de Montagem">

  <h4>Resultado da Simulação</h4>
  <p>O display LCD exibirá mensagens de acordo com a leitura dos sensores. Os LEDs acenderão em resposta a determinadas entradas, demonstrando o conceito de I/O em sistemas de computadores.</p>
</details>

<details>
  <summary>Explicação Técnica</summary>
  <p>O sistema utiliza sensores (PIR e temperatura) como dispositivos de entrada. O Arduino processa os sinais dos sensores e envia comandos para os dispositivos de saída (display LCD, LEDs). O código é responsável por interpretar os dados dos sensores e atualizar as saídas em tempo real.</p>

  <h4>Principais Trechos do Código</h4>
  cpp
  Wire.requestFrom(8, 1);  // Solicita dados do sensor
  if (Wire.available()) {
      int state = Wire.read();
      lcd1.print("Movimento detectado");
  }

</details> 

<details> <summary>Autores e Contribuições</summary> <ul> <li><strong>Edmar Pereira</strong> - Implementação do sistema e desenvolvimento do código.</li> <li><strong>Ronyldo</strong> - Montagem do circuito e testes no Tinkercad.</li> </ul> <p>Professor responsável: <strong>Moisés</strong> - Disciplina de Organização de Computadores no IFRN.</p> </details> <details> <summary>Conclusão</summary> <p>Este projeto proporcionou uma melhor compreensão sobre o papel dos dispositivos de Entrada e Saída (I/O) em sistemas computacionais. A prática no Tinkercad e a programação do Arduino reforçaram os conceitos discutidos em sala de aula, tornando a teoria mais palpável.</p> <h4>Aprendizados</h4> <ul> <li>Uso do Arduino para integrar sensores e displays.</li> <li>Comunicação I2C para leitura de dados dos sensores.</li> <li>Importância da sincronização entre entrada e saída em sistemas embarcados.</li> </ul> </details> <details> <summary>Referências</summary> <ul> <li><a href="https://www.arduino.cc/">Site Arduino</a></li> <li><a href="https://www.tinkercad.com/">Documentação do Tinkercad</a></li> <li>Livros e artigos relacionados à Organização de Computadores.</li> </ul> </details>
