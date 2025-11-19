# Wakfu Detona - Game

Pequeno jogo de combinar ícones em grade 9x9. Arraste e solte peças para formar linhas ou colunas de 3 ícones iguais, marque pontos e jogue contra o tempo.

## Estrutura do projeto
- [wakfu.html](wakfu.html) — página principal do jogo.
- [estilo.css](estilo.css) — estilos da interface.
- [estilo.js](estilo.js) — lógica do jogo (drag & drop, timer, geração e colisão).
- [icons_game/](icons_game/) — pasta com ícones (.png) usados no jogo.
- [.vscode/settings.json](.vscode/settings.json) — configurações do Live Server.

## Como executar
1. Abra [wakfu.html](wakfu.html) em um navegador.
2. Recomenda-se usar o Live Server do VSCode (porta definida em [.vscode/settings.json](.vscode/settings.json)) para recarregamento automático.

## Como jogar
- Arraste uma peça e solte em uma célula adjacente (esquerda, direita, cima, baixo).
- Forme uma sequência de 3 ícones iguais (linha ou coluna) para "crush" e ganhar pontos.
- O tempo inicial é mostrado em [wakfu.html](wakfu.html); o jogo termina quando o tempo acaba.

## Pontuação e regras principais
- Cada combinação de 3 ícones concede 30 pontos (implementado em [`crushThree`](estilo.js)).
- O jogo utiliza um timer controlado por [`startTimer`](estilo.js) e encerra via [`endGame`](estilo.js).
- Movimentos que não resultam em uma combinação válida são revertidos (ver [`checkValid`](estilo.js)).

## Principais funções (onde olhar na lógica)
- [`startGame`](estilo.js) — inicializa o tabuleiro e eventos de drag.
- [`startTimer`](estilo.js) — inicia o cronômetro.
- [`crushThree`](estilo.js) — detecta e remove trincas.
- [`slideWakfu`](estilo.js) — faz os ícones caírem após remoção.
- [`generateWakfu`](estilo.js) — gera novos ícones no topo.
- [`checkValid`](estilo.js) — valida se há combinação após um movimento.
- [`endGame`](estilo.js) — encerra o jogo e remove eventos.

## Possíveis melhorias
- Implementar combinações de 4/5 com pontuação diferenciada.
- Suavizar animações (transições CSS) para queda e remoção.
- Salvar melhores pontuações localmente.
- Ajustar responsividade para telas menores.

## Licença
Projeto simples de exemplo — adapte e use conforme necessário.
