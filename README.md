# Ascii-studio
Transforme imagens em arte ASCII animada diretamente no navegador.

O ASCII Studio é uma ferramenta web que converte imagens em uma composição de caracteres de texto, permitindo personalizar a aparência, animação, cores e resolução da arte. O resultado pode ser exportado como uma página HTML independente ou como um GIF animado.

Preview

Converta uma imagem em uma textura de texto animada.

Live Demo: ASCII Studio

Funcionalidades
Conversão de imagens para ASCII Art
Animação horizontal dos caracteres
Personalização do padrão de caracteres
Controle do tamanho da fonte
Controle da velocidade da animação
Ajuste da quantidade de colunas
Correção de proporção da imagem
Controle de brilho mínimo
Suporte a:
Cores originais da imagem
Cor personalizada
Controle da intensidade mínima dos caracteres
Upload de imagens por arquivo ou arrastar e soltar
Exportação da ASCII Art como arquivo HTML
Exportação da animação como GIF
Interface totalmente baseada em HTML, CSS e JavaScript
Tecnologias
HTML5
CSS3
JavaScript
Canvas 2D API
gif.js
Web Workers
Como funciona

O processo de conversão é realizado utilizando o Canvas 2D API.

O usuário envia uma imagem.
A imagem é redimensionada para a quantidade de colunas definida.
O Canvas analisa os pixels da imagem.
O brilho de cada pixel é calculado utilizando os canais RGB.
Cada pixel é convertido em um caractere do padrão definido.
A cor e a transparência do caractere são determinadas a partir do pixel original.
Os caracteres são renderizados novamente no Canvas.
A animação é criada deslocando o padrão de caracteres horizontalmente.

A luminância utilizada na conversão é calculada aproximadamente como:

brightness = R × 0.299 + G × 0.587 + B × 0.114
Exportação
HTML

A opção Baixar HTML do resultado gera uma página HTML independente contendo:

Canvas
Imagem incorporada em Base64
Configurações utilizadas
Código JavaScript responsável pela animação

Isso permite abrir o resultado posteriormente sem precisar do ASCII Studio original.

GIF

A opção Gerar GIF utiliza o gif.js para capturar múltiplos frames da animação e gerar um GIF.

O processamento utiliza um Web Worker para evitar bloquear a interface durante a renderização.

Estrutura
ASCII-Studio/
├── index.html
├── gif.worker.js
├── miku.ico
└── README.md
Executando localmente

Clone o repositório:

git clone https://github.com/lscski/ascii-studio.git

Entre na pasta:

cd ascii-studio

Depois abra o index.html no navegador ou utilize uma extensão como Live Server no VS Code.

Deploy

O projeto pode ser hospedado diretamente em serviços de hospedagem estática, como o Netlify.

Live: lscski-ascii-studio.netlify.app

Autor

Desenvolvido por @lscski.

Redes sociais
X: @lscski
Instagram: @lascoski__
Discord: lscsk
Licença

Este projeto está disponível para fins de estudo e uso pessoal. Consulte o repositório para informações adicionais sobre licença e distribuição.
