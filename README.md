# Laboratório Montador Daedalus — Ahmes e Ramses

Resolução dos 7 exercícios do laboratório "Montador Daedalus" (Sistemas de Computação 1 de Automação, IFSP Hortolândia), escritos no montador **Daedalus** para os processadores didáticos **Ahmes** e **Ramses**.

**Autor:** Gabriel Cabral Wallendzu — HT3080251
**Professor:** Carlos Eduardo Pagani

## Exercícios

| # | Descrição | Ahmes | Ramses |
|---|---|---|---|
| 1 | Zerar registradores A, B e X (individual e todos) | `Ahmes/Ex1-Ahmes.ahd` | `Ramses/Ex1-Ramses.rad` |
| 2 | Soma de 8 e 16 bits com flag de overflow (FFh / 0) | `Ahmes/Ex2-Ahmes.ahd` | `Ramses/Ex2-Ramses.rad` |
| 3 | Zerar n posições consecutivas de memória | `Ahmes/Ex3-Ahmes.ahd` | `Ramses/Ex3-Ramses.rad` |
| 4 | Maior entre três variáveis | `Ahmes/Ex4-Ahmes.ahd` | `Ramses/Ex4-Ramses.rad` |
| 5 | Complemento de dois e sinal-magnitude (byte e palavra) | `Ahmes/Ex5-Ahmes.ahd` | `Ramses/Ex5-Ramses.rad` |
| 6 | Nome em ASCII a partir de uma posição de memória | `Ahmes/Ex6-Ahmes.ahd` | `Ramses/Ex6-Ramses.rad` |
| 7 | Multiplicação de dois números positivos | `Ahmes/Ex7-Ahmes.ahd` | `Ramses/Ex7-Ramses.rad` |

## Como executar

1. Abra o Daedalus e escolha a **Máquina Alvo** (Ahmes ou Ramses).
2. Abra o arquivo de código-fonte (`.ahd` para Ahmes, `.rad` para Ramses) no Daedalus, ou cole o conteúdo no **Código Fonte**, e monte o programa.
3. Carregue no simulador, execute e confira a memória e os registradores.

## Arquivos

- `.ahd` (Ahmes) e `.rad` (Ramses): código-fonte do Daedalus.
- `.map` e `.mem`: arquivos gerados na montagem (mapa de rótulos/endereços e imagem da memória), usados pelo simulador.

## Convenções

- Variáveis a partir da posição 128 (`org 128`); código a partir da posição 0 (`org 0`).
- Comentários após `;` explicando cada etapa.

## Testes realizados

Todos os programas foram montados no Daedalus e executados nos simuladores Ahmes e Ramses, com a memória e os registradores conferidos ao final. Todos os exercícios foram aprovados nas duas máquinas.

| Ex. | Entradas de teste | Saídas verificadas | Status |
|---|---|---|---|
| 1 | Ramses: A=5, B=6, X=7. Ahmes: VAR1=5, VAR2=9 | A, B e X = 0; VAR1 = VAR2 = 0 | Aprovado |
| 2 | 8 bits: 200+100. 16 bits: 02C8h+0164h | OV8=FFh; S8=2Ch; SH:SL=04h:2Ch; OV16=00h | Aprovado |
| 3 | INI=150, N=5 | Posições 150–154 = 0; 155–157 = 6, 7, 8 | Aprovado |
| 4 | VA=3, VB=5, VC=14 | MAIOR=0Eh (14) | Aprovado |
| 5 | Byte=3; palavra=0003h | C2B=FDh; SMB=83h; C2H:C2L=FFh:FDh; SMH:SML=80h:03h | Aprovado |
| 6 | Destino=200 | A partir da posição 200: GABRIEL CABRAL WALLENDZU em ASCII | Aprovado |
| 7 | N1=4, N2=3 | RES=0Ch (12) | Aprovado |

## Divisão das tarefas (kanban)

Trabalho individual: todas as tarefas foram feitas por Gabriel Cabral Wallendzu.

| A fazer | Em andamento | Concluído |
|---|---|---|
| — | — | Ex. 1 a 7 (Ahmes e Ramses) |
| — | — | Repositório no GitHub e relatório |

## Relatório

O relatório completo está em `Relatorio_Daedalus_Ahmes_Ramses.docx`.

