# Prumo: produto e interface

Plataforma de estudos com IA para ENEM e concursos.

[![Status](https://img.shields.io/badge/status-em%20produção-success)](https://estudeprumo.com)
[![Web](https://img.shields.io/badge/web-Next.js%20%7C%20React-informational)](https://estudeprumo.com)

Este repositório é um estudo de caso: documenta o produto e a interface da Prumo. No site, eu
construo tudo: o visual, as telas e as funcionalidades. A segurança é do Victor e está no
estudo de caso dele, em [burnoutscript/prumo](https://github.com/burnoutscript/prumo).
O código-fonte é proprietário e não está aqui.

Produto no ar: https://estudeprumo.com

![Painel do aluno](docs/painel.png)

## O problema

Estudar para ENEM e concurso é uma maratona de meses, e quase todo mundo desiste no meio. A
maioria das plataformas parece uma planilha cheia de questões: funciona para quem já tem
disciplina, mas não ajuda quem precisa de um motivo para abrir o site hoje de novo.

## A ideia

Fazer o estudo parecer um jogo que dá vontade de abrir todo dia, sem deixar de ser estudo
sério. Por isso a Prumo tem visual de desenho animado, um mascote que reage ao aluno, XP,
ligas e torneios, e cada tela tenta levar a pessoa à próxima questão pelo caminho mais curto.

| | |
|---|---|
| Status | Em produção desde agosto de 2026, com usuários e pagamentos reais |
| Meu papel | Cofundador e CTO. Construo o site: produto, visual, telas e funcionalidades |
| Time | Dois fundadores: eu e o [Victor Candido](https://github.com/burnoutscript), que cuida da segurança |

## O que construí

| Área | Funcionalidades |
|---|---|
| Estudo | Simulados, flashcards, caderno de erros, objetivos e Modo Foco |
| Redação | Corretor de redação com IA, que também lê redação escrita à mão por foto |
| Jogo | XP e níveis, sequência de dias, conquistas, missões diárias, prova chefe, avatar e loja de itens |
| Social | Duelo entre alunos, ranking, ligas, torneios, times, convites, perfil público e integração com o Discord |
| Negócio | Planos com Pix, notificações push, resumo semanal e relatório em PDF |

| Simulado | Redação |
|---|---|
| ![Novo simulado](docs/simulado.png) | ![Redação](docs/redacao.png) |

## Decisões de interface

#### Design system próprio, sem Tailwind

Cores, espaçamentos, bordas e sombras são variáveis CSS num lugar só. O visual de desenho
animado (borda grossa, sombra sólida, cantos bem redondos) depende de detalhes que se repetem
em centenas de telas, e com tokens próprios uma mudança vale para o site inteiro.

#### Um mascote que olha para o aluno

O mascote aparece no login, no painel e nas comemorações, com várias poses. As pupilas não
fazem parte da imagem: são um SVG por cima que segue o mouse. Assim uma pose só serve para
qualquer direção do olhar. Dessa parte nasceu o meu projeto aberto
[mascote-vivo](https://github.com/nullfeel/mascote-vivo), com código novo e um mascote novo.

#### Comemorar o que o aluno fez

Terminar um simulado, subir de liga ou manter a sequência de dias gera uma comemoração e um
card pronto para compartilhar no Instagram. É o tipo de detalhe que faz a pessoa voltar amanhã
e ainda traz amigos.

#### Animação que respeita quem não quer animação

Quem ativa "reduzir movimento" no sistema vê a Prumo parada, com as mesmas informações. As
animações são enfeite, nunca o único jeito de entender a tela.

#### Mostrar antes de explicar

A página inicial mostra telas de verdade do produto e uma demonstração que dá para usar sem
criar conta. O vídeo de divulgação também é feito em código, com Remotion, usando as mesmas
telas.

## Stack da interface

| Camada | Tecnologia |
|---|---|
| Web | Next.js 16 (App Router), React 19, TypeScript |
| Estilo | CSS com design system próprio |
| Animação | GSAP e CSS |
| Estado | Zustand |
| Dados | Supabase |
| Vídeo | Remotion |
| Testes | Vitest |
| Erros | Sentry |

Programo com agentes de código no dia a dia (Claude Code, Cursor, OpenCode e Kimi), do
primeiro rascunho ao teste.

## Contato

Marcos Alan, cofundador e CTO · [GitHub](https://github.com/nullfeel) ·
[LinkedIn](https://www.linkedin.com/in/marcos-alan-passos-pereira-7a7a9b3b4/)

<sub>Código-fonte proprietário. Este repositório contém apenas documentação pública do projeto.</sub>
