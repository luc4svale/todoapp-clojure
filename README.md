# Todo List em Clojure e ClojureScript

Gerenciador de tarefas full-stack desenvolvido na disciplina Introdução à Programação Funcional, do curso de Engenharia da Computação da UFMA. O projeto segue o [tutorial de Clojure e ClojureScript](https://lambdageo-edu.github.io/lambdageo-tutorials/clojure/) do material didático da disciplina e acrescenta melhorias de organização e de interface.

## Sumário

- [Vídeo de apresentação](#vídeo-de-apresentação)
- [Dupla](#dupla)
- [Funcionalidades](#funcionalidades)
- [Requisitos](#requisitos)
- [Como usar](#como-usar)
- [Documentação](#documentação)
- [Uso de IA](#uso-de-ia)
- [Licença](#licença)

## Vídeo de apresentação

[Vídeo de apresentação no Google Drive](https://drive.google.com/file/d/1eLDs0s-7GPhdWyPhbkheGEcElEixymv6/view?usp=drive_link)

## Dupla

- Antonio Lucas da Silva Vale
- Izadora de Paula Santos Lima

## Funcionalidades

A aplicação permite criar tarefas, marcá-las como concluídas e filtrá-las entre pendentes e concluídas. Para excluir uma tarefa, é preciso confirmar a exclusão. As tarefas são salvas em SQLite e persistem após o reinício do servidor.

O backend usa Clojure com Ring, Reitit e next.jdbc. O frontend usa ClojureScript com Reagent e Shadow-CLJS.

## Requisitos

Java 11 ou superior, Clojure CLI 1.11 ou superior, Node.js 18 ou superior e Git.

## Como usar

```bash
git clone https://github.com/luc4svale/todoapp-clojure.git
cd todoapp-clojure
npm install
```

Em um terminal, suba o backend na porta 3000.

```bash
clj -M:run
```

Na primeira execução, o Clojure baixa as dependências e cria o banco `prod.db`. O backend está pronto quando aparece `Servidor iniciado na porta 3000`.

Em outro terminal, suba o frontend na porta 8000.

```bash
npx shadow-cljs watch app
```

Depois de `Build completed`, a aplicação abre em http://localhost:8000. Os dois terminais precisam continuar abertos.

Se o `clj` pedir o `rlwrap`, troque `clj` por `clojure` nos comandos.

## Documentação

- [Arquitetura](docs/architecture.md), com as pastas, os módulos e o banco
- [API](docs/api.md), com as rotas e exemplos de requisição e resposta
- [Decisões de processo](docs/decisions.md), com as diferenças em relação ao tutorial e as melhorias

## Uso de IA

O projeto foi desenvolvido com auxílio do Claude, assistente de IA da Anthropic, no modelo Opus 5.5, pelo claude.ai. A ferramenta foi usada para revisar o tutorial em busca de inconsistências antes do desenvolvimento, para propor a divisão das tarefas entre a dupla e as mensagens dos commits, para prototipar o design final da interface e para escrever a documentação, incluindo este README. Cada commit foi testado antes do envio ao repositório.

## Licença

MIT, conforme o arquivo [LICENSE](LICENSE).
