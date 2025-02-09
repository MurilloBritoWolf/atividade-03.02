Descrição da Atividade – Controle e Comunicação com Microcontroladores
Nesta atividade prática, os alunos irão desenvolver um projeto utilizando a placa BitDogLab, explorando conceitos fundamentais de comunicação serial (UART e I2C), interrupções, e controle de LEDs.

Objetivo Geral
Criar um sistema interativo que permita a entrada de caracteres via Serial Monitor, controle de LEDs por meio de botões físicos e exibição de informações em um display SSD1306.

Componentes Utilizados
Matriz 5x5 WS2812 (LEDs endereçáveis, GPIO 7).
LED RGB (conectado às GPIOs 11, 12 e 13).
Botão A (conectado à GPIO 5).
Botão B (conectado à GPIO 6).
Display OLED SSD1306 (conectado via I2C, GPIO 14 e 15).
Como Funciona o Código?
O código utiliza bibliotecas específicas para comunicação e controle dos periféricos. Todas as bibliotecas necessárias estão na pasta bibliotecas.

Configuração Inicial

Importação das bibliotecas para controle de LEDs, botões, display SSD1306 e comunicação serial.
Inicialização da UART para receber caracteres via Serial Monitor.
Configuração do display SSD1306 via I2C.
Definição das GPIOs para os LEDs e botões.
Manipulação de Caracteres

O código recebe caracteres enviados via Serial Monitor (VS Code).
O caractere é exibido no display OLED.
Se o caractere for um número (0-9), um símbolo correspondente é mostrado na matriz de LEDs WS2812.
Interrupções e Controle de Botões

Botão A: Alterna o estado do LED Verde e exibe mensagens no display e no Serial Monitor.
Botão B: Alterna o estado do LED Azul e também exibe mensagens no display e no Serial Monitor.
Para evitar múltiplas leituras indesejadas, é aplicado um filtro de debounce via software.
Uso das Bibliotecas

Biblioteca para o display SSD1306: Facilita o envio de caracteres ao display via I2C.
Biblioteca para LEDs WS2812: Permite o controle individual de cada LED na matriz.
Biblioteca de interrupções (IRQ): Garante resposta rápida ao pressionamento dos botões.
Biblioteca Serial (UART): Gerencia o envio e recepção de caracteres via Serial Monitor.
Requisitos Técnicos
Interrupções (IRQ): O controle dos botões deve ser feito por rotinas de interrupção.
Debounce via Software: Implementação obrigatória para evitar múltiplos acionamentos.
Controle de Diferentes Tipos de LEDs: LEDs comuns e WS2812 devem ser manipulados corretamente.
Uso do Display OLED: Exibição de maiúsculas e minúsculas utilizando o protocolo I2C.
Comunicação Serial UART: Envio e recepção de dados via Serial Monitor do VS Code.
Código bem estruturado e comentado: Para facilitar a compreensão e manutenção do projeto.
Vídeo Demonstrativo
Para melhor compreensão do projeto, assista ao vídeo disponível no link:
📺 [Inserir link do YouTube aqui]

Este projeto combina hardware e software para consolidar conhecimentos em comunicação serial, controle de periféricos e manipulação de interrupções, promovendo uma experiência prática e didática no uso de microcontroladores. 🚀