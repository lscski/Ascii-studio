# ASCII Studio

<p align="center">
  <img src="./miku.ico" width="80" alt="ASCII Studio">
</p>

<h3 align="center">Transforme imagens em arte ASCII animada.</h3>

<p align="center">
  Uma ferramenta web para converter imagens em composições de caracteres,
  personalizar cores e animações e exportar o resultado como HTML ou GIF.
</p>

<p align="center">
  <a href="https://lscski-ascii-studio.netlify.app/">
    <strong>Live Demo</strong>
  </a>
</p>

---

## Sobre o projeto

O **ASCII Studio** é uma ferramenta web desenvolvida para transformar imagens em **ASCII Art animada**, utilizando caracteres de texto para reproduzir os detalhes, cores e luminosidade da imagem original.

O projeto utiliza a **Canvas 2D API** para processamento e renderização dos pixels, permitindo gerar a arte em tempo real diretamente no navegador.

A proposta é combinar uma interface minimalista com controles que permitem personalizar completamente o resultado final.

---

## Funcionalidades

- Conversão de imagens para ASCII Art
- Animação dos caracteres
- Personalização do padrão de caracteres
- Controle do tamanho da fonte
- Controle da velocidade da animação
- Controle da quantidade de colunas
- Correção de proporção da imagem
- Controle do brilho mínimo
- Suporte às cores originais da imagem
- Suporte a cor personalizada
- Controle da intensidade mínima dos caracteres
- Upload de imagens
- Drag and Drop
- Exportação da arte como HTML
- Exportação da animação como GIF
- Processamento de GIF utilizando Web Worker

---

## Controles

| Controle | Descrição |
|---|---|
| **Padrão de texto** | Define os caracteres utilizados na arte |
| **Tamanho da fonte** | Ajusta o tamanho dos caracteres |
| **Velocidade de rolagem** | Controla a velocidade da animação |
| **Colunas** | Define a resolução horizontal da ASCII Art |
| **Correção de proporção** | Ajusta a proporção dos caracteres |
| **Limiar mínimo de brilho** | Remove pixels abaixo de determinado brilho |
| **Cor real** | Mantém as cores originais da imagem |
| **Cor fixa** | Utiliza uma única cor para toda a arte |
| **Intensidade mínima** | Define a transparência mínima dos caracteres |

---

## Como funciona

O processo de conversão utiliza o **Canvas 2D API** para analisar os pixels da imagem.

### 1. Upload

O usuário fornece uma imagem através do upload ou arrastando o arquivo para a área indicada.

### 2. Redimensionamento

A imagem é redimensionada de acordo com a quantidade de colunas selecionada.

### 3. Análise dos pixels

Cada pixel é analisado individualmente para obter seus valores:

```text
R = Red
G = Green
B = Blue
A = Alpha
