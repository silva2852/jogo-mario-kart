🎮 Mario Kart

Um jogo de combate por turnos inspirado em clássicos arcade, executado diretamente no terminal com Node.js. Dois jogadores escolhem personagens, utilizam itens especiais e enfrentam desafios em cenários aleatórios até restar apenas um vencedor.

🧠 Sobre o Projeto

Este projeto foi criado com foco em mecânicas simples de RPG e interação via terminal, explorando conceitos importantes de programação em JavaScript.

Durante a partida, os jogadores precisam combinar estratégia, sorte e gerenciamento de recursos para vencer os confrontos.

O projeto trabalha principalmente com:

Estruturas de dados
Programação assíncrona
Lógica de turnos
Manipulação de entrada no terminal
Eventos aleatórios
⚙️ Tecnologias Utilizadas
Node.js
JavaScript (ESM)
Módulos nativos do Node:
readline/promises
ANSI Escape Codes para estilização no terminal
🏗️ Organização do Projeto
1. Entrada de Dados

A comunicação com o jogador acontece diretamente pelo terminal utilizando o módulo readline/promises.

const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});

Isso permite capturar respostas de forma assíncrona sem bloquear a execução do jogo.

2. Estrutura dos Personagens

Os personagens são armazenados em objetos contendo atributos específicos para cada situação da partida.

const fighters = [
  { name: "Hero", speed: 4, skill: 3, power: 3, hp: 12 }
];
Atributos disponíveis
speed → vantagem em terrenos rápidos
skill → melhor desempenho técnico
power → dano em combate
hp → quantidade de vida
special → habilidade exclusiva
3. Sistema de Itens

Durante a partida, os jogadores podem encontrar itens aleatórios com diferentes efeitos.

const items = [
  { name: "Poção", type: "heal" }
];
Tipos de item
heal → recupera vida
damage → aplica dano
buff → melhora atributos temporariamente
debuff → enfraquece o adversário

Cada jogador possui limite de espaço no inventário, incentivando escolhas estratégicas.

4. Mecânica de Rodadas

Cada rodada segue uma sequência dinâmica:

Chance de obter itens
Sorteio do cenário
Escolha de ações
Rolagem de dados
Cálculo do resultado
Aplicação de dano
Tipos de cenário
Sprint → usa velocidade
Arena → usa força
Desafio Técnico → usa habilidade

O resultado da rodada é calculado com:

dado + atributo + modificadores
5. Sistema de Confronto

As batalhas utilizam dano variável dependendo do tipo de terreno.

Ataque comum → reduz 1 HP
Combate direto → reduz 2 HP

Habilidades especiais também podem alterar resultados em caso de empate ou vantagem específica.

6. Rolagem de Dados

O jogo simula visualmente uma rolagem para deixar a experiência mais dinâmica.

for (let i = 0; i < 8; i++) {
  value = Math.floor(Math.random() * 6) + 1;
}

Essa animação gera uma sensação mais interativa dentro do terminal.

7. Fluxo Assíncrono

O controle do jogo utiliza:

async/await
Promises
setTimeout

Esses recursos ajudam na fluidez das ações e criam pausas entre eventos importantes.

▶️ Executando o Projeto
1. Instale o Node.js

Recomendado: versão 18 ou superior.

2. Salve o arquivo principal
battle-arena.mjs
3. Execute no terminal
node battle-arena.mjs
🎮 Como Funciona
Escolha os personagens dos jogadores
Utilize itens estrategicamente
Aproveite vantagens do cenário
Derrote o oponente antes que sua vida chegue a zero

O último sobrevivente vence a partida.

🚀 Possíveis Expansões
Sistema PvE com IA
Multiplayer online
Ranking de jogadores
Interface gráfica
Efeitos sonoros
Novos personagens e habilidades
Sistema de progressão
📚 Conceitos Praticados

Este projeto é útil para estudar:

Programação assíncrona
Estruturas de objetos e arrays
Manipulação de terminal
Organização de lógica de jogos
Controle de fluxo em JavaScript
🏁 Encerramento

O Terminal Battle Arena demonstra como é possível criar experiências divertidas utilizando apenas Node.js e lógica de programação, sem necessidade de engines gráficas complexas.

Mesmo sendo um projeto simples, ele reúne conceitos importantes de desenvolvimento e pode servir como base para jogos maiores no futuro.
