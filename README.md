Aqui está a documentação estruturada seguindo o modelo que você forneceu. Isso garante clareza, organização e facilidade de entendimento para os participantes da atividade.  

---

# **Projeto de Controle e Comunicação com Microcontroladores**  

Este repositório contém um projeto prático utilizando a placa **BitDogLab**, explorando conceitos essenciais de **comunicação serial (UART e I2C)**, manipulação de **interrupções**, **controle de LEDs** e **exibição de informações em um display OLED SSD1306**.  

O objetivo central é desenvolver um **sistema interativo** que permite a entrada de caracteres via **Serial Monitor**, controle de LEDs por **botões físicos**, e exibição dinâmica de informações em um **display OLED**.  

---

## **Eletrônicos Utilizados**  

### **Componentes Principais**  
- **BitDogLab:** Microcontrolador utilizado para comunicação e controle.  
- **Matriz 5x5 WS2812:** LEDs endereçáveis conectados ao **GPIO 7**.  
- **LED RGB:** Conectado aos **GPIOs 11, 12 e 13**.  
- **Botão A:** Conectado ao **GPIO 5**, usado para alternar o LED verde.  
- **Botão B:** Conectado ao **GPIO 6**, usado para alternar o LED azul.  
- **Display OLED SSD1306:** Conectado via **I2C (GPIOs 14 e 15)** para exibição de caracteres.  

---

## **Descrição da Atividade**  

### **Configuração Inicial**  
O código faz uso de bibliotecas específicas para controle de periféricos e comunicação. Todas as bibliotecas necessárias estão disponíveis na pasta **bibliotecas** do projeto. A configuração inicial segue os seguintes passos:  

1. **Importação das bibliotecas** para LEDs, botões, display SSD1306 e comunicação serial.  
2. **Inicialização da UART** para recepção de caracteres via **Serial Monitor (VS Code)**.  
3. **Configuração do display SSD1306** para comunicação via **I2C**.  
4. **Definição dos GPIOs** associados aos LEDs e botões físicos.  

---

### **Manipulação de Caracteres via Serial**  
- O sistema recebe **caracteres** enviados pelo **Serial Monitor** e os exibe no **display OLED**.  
- Se o caractere for um **número (0-9)**, um **símbolo correspondente** é exibido na **matriz de LEDs WS2812**.  

### **Interrupções e Controle de Botões**  
Para um controle eficiente e responsivo, os botões são gerenciados através de **interrupções (IRQ)** e filtragem de **debounce via software**.  

- **Botão A (GPIO 5):**  
  - Alterna o estado do **LED verde**.  
  - Exibe mensagens no **display** e no **Serial Monitor**.  
- **Botão B (GPIO 6):**  
  - Alterna o estado do **LED azul**.  
  - Exibe mensagens no **display** e no **Serial Monitor**.  

Durante a execução, o sistema ignora múltiplas leituras acidentais dos botões devido à implementação do **debounce**.  

---

## **Uso das Bibliotecas**  
O código utiliza bibliotecas especializadas para otimizar o funcionamento dos componentes:  

- **Biblioteca SSD1306:** Facilita a comunicação com o display OLED via **I2C**.  
- **Biblioteca WS2812:** Permite controle preciso dos **LEDs endereçáveis** da matriz 5x5.  
- **Biblioteca IRQ (Interrupções):** Garante resposta rápida ao pressionamento dos botões.  
- **Biblioteca UART:** Gerencia **envio e recepção** de caracteres via **Serial Monitor**.  

---

## **Requisitos Técnicos**  
- **Interrupções (IRQ):** O controle dos botões deve ser realizado por **rotinas de interrupção** para minimizar latência.  
- **Debounce via Software:** Implementação obrigatória para evitar múltiplos acionamentos.  
- **Controle de LEDs Diferenciados:** Manipulação tanto de **LEDs comuns** quanto da **matriz WS2812**.  
- **Uso do Display OLED:** Exibição de **caracteres alfanuméricos** via **I2C**.  
- **Comunicação Serial UART:** Envio e recepção de dados pelo **Serial Monitor do VS Code**.  
- **Código Estruturado e Comentado:** Facilita compreensão e manutenção futura do projeto.  

---

## **Instruções de Uso**  

### **1️⃣ Pré-requisitos**  
- Instalar e configurar o **Pico SDK**.  
- Acessar o **VS Code** e abrir o **Serial Monitor** para enviar caracteres.  
- Conectar os componentes conforme as especificações.  

### **2️⃣ Execução do Projeto**  
- **Carregar o código-fonte** na placa **BitDogLab**.  
- **Observar as reações:**  
  - **LEDs alternam estados** ao pressionar os botões.  
  - **Caracteres aparecem no display OLED** conforme inseridos no **Serial Monitor**.  
  - **Símbolos específicos são desenhados na matriz WS2812** ao inserir números.  

---

## **Demonstração em Vídeo**  
📺 Para visualizar o funcionamento do projeto na prática, assista ao vídeo disponível no link:  
[**(https://youtube.com/shorts/JNpzfpx5yM8?feature=share)**]  

---

## **Considerações Finais**  
Este projeto combina **hardware e software** para consolidar o aprendizado sobre **comunicação serial, interrupções, debounce e controle de periféricos**. O uso da **BitDogLab** permite um ambiente robusto para simulações e desenvolvimento de sistemas embarcados interativos.  

Além disso, a implementação prática reforça conceitos fundamentais, como:  
✅ Manipulação eficiente de **UART e I2C**.  
✅ Uso de **interrupções** para controle responsivo.  
✅ Aplicação de **debounce via software**.  
✅ Integração de **diferentes tipos de LEDs** e **displays**.  

Este é um excelente exercício para aprimorar habilidades em **sistemas embarcados** e **microcontroladores**, preparando os alunos para projetos mais complexos no futuro. 🚀  

---

**🔧 Desenvolvido por João Murillo Brito Taveira - Grupo  4 - Subgrupo 6.**
