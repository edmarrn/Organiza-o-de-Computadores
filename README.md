# Projeto de Organização de Computadores: Entrada/Saída (I/O)

## Índice
- [Descrição](#descrição)
- [Objetivos](#objetivos)
- [Requisitos](#requisitos)
- [Como Executar](#como-executar)
- [Demonstração](#demonstração)
- [Explicação Técnica](#explicação-técnica)
- [Autores e Contribuições](#autores-e-contribuições)
- [Conclusão](#conclusão)
- [Referências](#referências)

## Descrição
Este projeto aborda os conceitos de Entrada/Saída (I/O) no contexto da Organização de Computadores. Focamos no desenvolvimento e simulação de um sistema que demonstra a integração entre sensores e dispositivos de saída, mostrando como a comunicação entre hardware e software é essencial para sistemas computacionais modernos.

## Objetivos
- Compreender o funcionamento dos dispositivos de Entrada e Saída (I/O).
- Desenvolver um protótipo utilizando sensores (entrada) e displays/LEDs (saída).
- Simular a comunicação entre os componentes para reforçar conceitos teóricos da disciplina.

## Requisitos
Para reproduzir este projeto, você precisará de:
- Conta no Tinkercad para simulação de circuitos.
- Arduino IDE para programação do microcontrolador.
- Componentes: LEDs, resistores, sensores (PIR, temperatura), display LCD.
- Bibliotecas Arduino:
  - `Adafruit_LiquidCrystal`
  - `Wire.h`

## Como Executar
1. Acesse o Tinkercad e faça login com sua conta.
2. Importe o arquivo do circuito disponível no [link do Tinkercad](https://www.tinkercad.com/).
3. No Tinkercad, carregue o código fornecido em `codigo.ino` e execute a simulação.
4. No Arduino IDE, instale as bibliotecas necessárias (`Adafruit_LiquidCrystal`, `Wire`).
5. Conecte os componentes conforme o esquema abaixo:

   ![Esquema de ligação](imagens/esquema_ligacao.png)

6. Faça upload do código para o Arduino e observe os resultados no display e LEDs.

## Demonstração
### Esquema de Montagem
![Esquema](imagens/esquema.png)

### Resultado da Simulação
O display LCD exibirá mensagens de acordo com a leitura dos sensores. Os LEDs acenderão em resposta a determinadas entradas, demonstrando o conceito de I/O em sistemas de computadores.

## Explicação Técnica
O sistema utiliza sensores (PIR e temperatura) como dispositivos de entrada. O Arduino processa os sinais dos sensores e envia comandos para os dispositivos de saída (display LCD, LEDs). O código é responsável por interpretar os dados dos sensores e atualizar as saídas em tempo real.

### Principais Trechos do Código
```cpp
Wire.requestFrom(8, 1);  // Solicita dados do sensor
if (Wire.available()) {
    int state = Wire.read();
    lcd1.print("Movimento detectado");
}
