[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/zHqjFsRx)
# Diagnóstico de retomada - Teoria da Computação

Esta atividade serve para mapear o que você já domina sobre linguagens formais, autômatos, gramáticas e computabilidade.

Responda individualmente. Use suas palavras. Se usar IA depois da primeira tentativa, registre o uso na seção 7.

## 1. Mapa do que eu lembro

Marque cada tópico como: lembro bem, lembro parcialmente, não lembro, nunca vi ou não tenho certeza.

- alfabeto: lembro bem
- cadeia: lembro bem
- linguagem: lembro parcialmente
- gramática: lembro parcialmente   
- autômato finito: lembro parcialmente
- linguagem regular: não lembro
- linguagem livre de contexto: lembro bem
- linguagem sensível ao contexto: não tenho certeza
- linguagem irrestrita: não lembro   
- hierarquia de Chomsky: nunca vi
- computabilidade: lembro parcialmente
- máquina de Turing: lembro parcialmente

## 2. Definições com exemplo

Explique, com suas palavras e com um exemplo simples, usando o alfabeto `Sigma = {a, b}`.

1. O que é um alfabeto?
   Um alfabeto é um conjunto de símbolos usados para formar palavras ou cadeias.
   Ex: Σ = {a, b} - nesse caso o alfabeto possui apenas os símbolos "a" e "b".
   
2. O que é uma cadeia?
   Uma cadeia é uma sequência de símbolos pertencentes ao alfabeto.
Exemplos usando Σ = {a, b}: “aab”, “abba”, “bb”.
Todas essas cadeias usam apenas símbolos do alfabeto.

3. O que é uma linguagem?
Uma linguagem é um conjunto de cadeias que seguem uma determinada regra.
Exemplo:L = {aa, ab, ba, bb}
Essa linguagem contém todas as cadeias de tamanho 2 formadas com “a” e “b”.

4. O que é uma gramática?
   Uma gramática é um conjunto de regras usadas para gerar cadeias de uma linguagem.
Exemplo simples:
S → aS | bS | ε
Essa gramática gera várias cadeias usando “a” e “b”, como:
a
ab
baba
aaabb
O símbolo ε representa a cadeia vazia.

## 3. Linguagens

Considere as linguagens:

```text
L1 = { w em {0,1}* | w termina com 01 }
L2 = { a^n b^n | n >= 0 }
L3 = { a^n b^n c^n | n >= 0 }
```

Para cada linguagem:

1. escreva três palavras que pertencem à linguagem;
L1 = 01, 101, 1101;
L2 = vazio, ab, aabb;
L3 = vazio, abc, aabbcc;

3. escreva duas palavras que não pertencem;
L1 = 10, 111;
L2 = aab, abb;
L3 = aabbc, abbcc;

4. diga, se souber, em qual classe ela provavelmente se encaixa;
L1 = linguagem regular;
L2 = linguagem livre de contexto;
L3 = linguagem livre de contexto;

5. explique o motivo em linguagem simples.
L1 = Basta verificar se a palavra termina com 01. Um autômato finito consegue fazer isso guardando apenas os últimos símbolos lidos.
l2 = A linguagem precisa ter a mesma quantidade de a e b, com todos os a antes dos b. Um autômato com pilha consegue contar os a e comparar com os b.
L3 = Ela exige a mesma quantidade de a, b e c. Uma pilha só não é suficiente para comparar três grupos ao mesmo tempo, então ela é mais complexa que uma linguagem livre de contexto.

Não há problema em dizer "não sei". Nesse caso, escreva o que te deixou em dúvida.

## 4. Autômato finito

Considere o autômato abaixo, sobre o alfabeto `{0,1}`:

```text
Estados: q0, q1, q2
Estado inicial: q0
Estado final: q2

Transições:
q0 --0--> q1
q0 --1--> q0
q1 --0--> q1
q1 --1--> q2
q2 --0--> q1
q2 --1--> q0
```

Responda:

1. Qual linguagem esse autômato parece reconhecer?
Cadeias que terminam com 01.

2. Execute manualmente as cadeias abaixo e diga se aceita ou rejeita:
   - `01` Aceita;
   - `101` Aceita;
   - `100` Rejeita
   - `1101` Aceita;
   - `111` rejeita

3. Monte uma tabela curta mostrando o caminho dos estados para pelo menos duas cadeias.

101:
| Símbolo lido | Estado atual |
| ------------ | ------------ |
| início       | q0           |
| 1            | q0           |
| 0            | q1           |
| 1            | q2           |

100:
| Símbolo lido | Estado atual |
| ------------ | ------------ |
| início       | q0           |
| 1            | q0           |
| 0            | q1           |
| 0            | q1           |

## 5. Gramática

Considere a gramática:

```text
S -> aS
S -> b
```

Responda:

1. Gere cinco cadeias produzidas por essa gramática.
b
ab
aab
aaab
aaaab

2. Descreva a linguagem em palavras.
Essa gramática gera cadeias formadas por zero ou mais letras a seguidas obrigatoriamente por uma letra b no final.

3. Essa gramática parece regular, livre de contexto ou outra classe? Justifique de forma simples.
Ela parece ser uma gramática regular.

## 6. Ponto de dificuldade

Escolha um tópico da lista inicial e escreva:

1. o que você entende dele;
Tipos de linguagens, eu sei que exitem diferentes tipos de linguagens, como linguagem regular, livre de contexto e sensível ao contexto e que cada uma tem um nível de dificuldade;
2. onde você se confunde;
Em classificar a qual tipo de exemplo o exemplo pertence.

3. que tipo de explicação ajudaria: Exemplos e explicações do motivo de cada linguagem ser oq é.
## 7. Uso de IA, se houver

Se você usou IA depois da primeira tentativa, registre:

```text
Pergunta feita:
Resumo da resposta:
Como eu verifiquei:
O que eu alterei na minha resposta:
O que ainda não entendi:
```

## Submissão no Moodle

Depois de finalizar, copie no Moodle:

```text
Repositório:
Commit final:
Autoavaliação: nível atual, maior dificuldade e tópico que precisa ser retomado.
```
