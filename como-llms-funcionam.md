---
layout: page
title: "Por Trás do Código: Como as LLMs Realmente Funcionam?"
tag: Inteligência Artificial
---

Modelos de Linguagem de Grande Escala (LLMs) como o ChatGPT, o Claude e o Gemini transformaram a forma como interagimos com computadores. Mas por trás das respostas fluentes e dos raciocínios sofisticados existe, essencialmente, álgebra linear aplicada em escala — bilhões de operações matemáticas traduzidas em diálogo coerente.

## O Que São os Bilhões de Parâmetros?

Quando você ouve que um modelo tem "70 bilhões de parâmetros", esses parâmetros são valores de ajuste calibrados durante o treinamento — pense neles como centenas de bilhões de pequenos botões de rádio, cada um afinado para capturar um padrão da linguagem. Trabalhando em conjunto, eles permitem que o modelo escreva código, traduza idiomas e resolva problemas complexos.

## Tokenização: Traduzindo Texto para Computadores

Antes de processar qualquer palavra, o modelo a divide em **tokens** — fragmentos menores que nem sempre coincidem com palavras completas. "Programar", por exemplo, pode virar `"program"` + `"ar"`. Essa fragmentação ajuda o modelo a identificar padrões entre palavras relacionadas como "programa" e "programação", reconhecendo raízes comuns.

## Embeddings: A Geometria do Significado

Cada token é convertido em um vetor de alta dimensão — um ponto num espaço geométrico onde palavras com significados parecidos ficam geograficamente próximas. O exemplo clássico: subtrair "Homem" de "Rei" e somar "Mulher" resulta num ponto muito próximo de "Rainha". O significado emerge da posição relativa no espaço, não de regras explícitas.

## A Revolução dos Transformers e a Atenção

Em 2017, o artigo *Attention Is All You Need* mudou tudo. A arquitetura **Transformer** introduziu o mecanismo de **Self-Attention**, que permite ao modelo processar todas as palavras de uma frase em paralelo e fazer cada palavra "olhar" para todas as outras, independentemente da distância entre elas.

### Como Funciona a Atenção?

O mecanismo opera com três componentes:

- **Query** — o que esta palavra está buscando?
- **Key** — o que esta palavra tem a oferecer?
- **Value** — que informação ela passa adiante?

Essa combinação permite ao modelo resolver corretamente qual substantivo realiza qual ação, mesmo em frases longas e ambíguas.

## O Refino em Camadas e o Feed Forward

Após a camada de atenção reunir as informações, os dados passam por redes **Feed Forward** que refinam ainda mais a representação. O GPT-3, por exemplo, empilha 96 dessas camadas em sequência — progredindo gradualmente de padrões gramaticais básicos até raciocínios mais abstratos e complexos.

## Treinamento: O Jogo de Adivinhação

O modelo aprende prevendo a próxima palavra em bilhões de textos. Cada erro é propagado de volta pela rede através de **Backpropagation**, ajustando incrementalmente cada parâmetro para que a próxima previsão seja um pouco melhor.

## Alinhamento: Fine-Tuning e RLHF

Após o treinamento base, o modelo passa por **fine-tuning** para se especializar em tarefas específicas. O passo seguinte é o **RLHF** (Aprendizado por Reforço com Feedback Humano): avaliadores humanos classificam respostas, e um "Modelo de Recompensa" aprende com essas avaliações para guiar o modelo a gerar respostas mais seguras, úteis e honestas.

## Por que a IA Inventa Coisas? (Alucinações)

O modelo não consulta um banco de dados de fatos — ele realiza previsões estatísticas sobre qual sequência de tokens é mais provável. O parâmetro **Temperature** controla o quanto de aleatoriedade é injetada nessa escolha. Quando a distribuição de probabilidade é incerta, o modelo pode "escolher" com confiança uma resposta incorreta. É o mecanismo que gera as famosas alucinações.

## O Contexto e a "Mesa de Escritório"

A **janela de contexto** define o quanto o modelo consegue "enxergar" de uma conversa de uma vez. Pense nela como uma mesa de trabalho: conforme a conversa avança, o que foi dito no início vai "caindo da mesa", e o modelo para de levar esse conteúdo em consideração.

## O Cenário Atual: Modelos Fechados vs. Open Source

Enquanto GPT (OpenAI), Claude (Anthropic) e Gemini (Google) dominam o mercado, alternativas open source ganham espaço rapidamente. O **DeepSeek R1** usa a arquitetura *Mixture of Experts* — ativando apenas uma fração dos parâmetros por vez para ganhar eficiência. Já o **MiniMax** aposta na *Lightning Attention*, suportando janelas de contexto de até 4 milhões de tokens.

---

Por trás de cada resposta de uma LLM não há consciência nem intenção — há matemática pura. A fronteira entre previsão de padrões e compreensão genuína segue sendo debatida, mas o fundamento permanece o mesmo: estatística em escala, empilhada em camadas, afinada com feedback humano.

*Artigo originalmente publicado por [Renato Carvalho](https://medium.com/@rdcar/por-trás-do-código-como-as-llms-realmente-funcionam-e3e8a0b6c396) no Medium.*
