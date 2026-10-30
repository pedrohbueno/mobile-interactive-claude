# Celular Desmontável

Um celular em 3D que você desmonta no navegador, no estilo *teardown*.

- **Arraste uma peça** para tirá-la do lugar.
- **Toque ou clique numa peça** para abrir uma ficha explicando o que ela é, para que serve, do que é feita e uma curiosidade.
- **Arraste o fundo** para girar o aparelho; use a pinça (celular) ou a roda do mouse para zoom.
- **Desmontar tudo** separa todas as camadas de uma vez; **Montar** coloca tudo de volta.
- **Peças** abre a lista com os 21 componentes.
- **Preços** vai direto para o gráfico de preço (processador, RAM, armazenamento, tela, bateria e câmeras).
- **Gráficos de preço** aparecem na ficha do processador, da RAM, do armazenamento, da tela, da bateria e das câmeras, com abas "mais potentes" e "custo-benefício" desde 2024.

## Sobre os preços

Fabricantes não publicam o preço das peças de celular. Por isso os gráficos misturam dois tipos de valor, sempre marcados:

- **Dado publicado** (linha cheia, ponto cheio): estimativas de analistas e da imprensa, com a fonte aparecendo ao tocar no ponto. Hoje cobrem os processadores topo de linha (Qualcomm, MediaTek, Apple, Exynos) e a variação trimestral do preço da RAM (TrendForce).
- **Valor de exemplo** (linha tracejada, ponto vazado): números ilustrativos para mostrar a tendência onde não há dado público. Não são preços reais.

Os dados ficam no objeto `PRECOS` dentro do `index.html`, e as fontes no objeto `FONTES`.

## Como rodar

Não precisa instalar nada. É um único arquivo, `index.html`, que carrega o [Three.js](https://threejs.org) pela internet.

- **Mais simples:** baixe o `index.html` e abra no navegador (Chrome, Edge, Firefox ou Safari).
- **Com servidor local (opcional):** na pasta do projeto, rode `python3 -m http.server` e abra `http://localhost:8000`.
- **Online pelo GitHub Pages:** em *Settings → Pages*, escolha a branch `main` e a pasta `/ (root)`. O site fica em `https://pedrohbueno.github.io/mobile-interactive-claude/`.

## Como funciona

- O modelo é feito de formas simples (caixas, cilindros e placas arredondadas) montadas em camadas, como num celular real: vidro, tela, componentes, placa-mãe, bateria, bobina e tampa traseira.
- Cada peça tem uma posição "montada" e um deslocamento usado no modo desmontado.
- As fichas ficam no objeto `INFO` dentro do `index.html`; para editar um texto ou incluir uma peça nova, é por lá.
