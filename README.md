\# Git Hooks - Padrão de Commits



Repositório centralizado para armazenar e reutilizar hooks do Git em diferentes projetos.



Este projeto utiliza o padrão \*\*Gitmoji + Conventional Commits\*\* para padronizar mensagens de commit, melhorar a organização do histórico e facilitar a manutenção dos repositórios.



\---



\## Objetivo



O objetivo deste repositório é manter hooks versionados e reutilizáveis, permitindo aplicar o mesmo padrão de commits em qualquer projeto, independentemente da IDE utilizada.



Funciona com:



\* IntelliJ IDEA

\* VSCode

\* Git Bash

\* Terminal

\* Qualquer ferramenta que utilize Git



\---



\## Padrão de Commit



Formato obrigatório:



```bash

emoji tipo(escopo): descrição

```



Exemplo:



```bash

✨ feat(core): adiciona validação inicial

```



Estrutura:



```bash

✨ feat(core): adiciona validação inicial

│   │    │       └── Descrição curta da alteração

│   │    └────────── Escopo da alteração

│   └─────────────── Tipo do commit

└─────────────────── Gitmoji

```



\---



\## Exemplos de Commits Válidos



```bash

🎉 chore(project): adiciona estrutura inicial

✨ feat(core): adiciona regra principal

🐛 fix(api): corrige retorno de erro

🔧 chore(config): ajusta configuração do projeto

📝 docs(docs): atualiza documentação

✅ test(tests): adiciona testes iniciais

♻️ refactor(utils): reorganiza funções auxiliares

🔒 fix(security): corrige validação de permissão

🗃️ feat(database): adiciona migration inicial

🚀 ci(ci): adiciona workflow de validação

```



\---



\## Exemplos de Commits Inválidos



```bash

ajustes

correção

feat: adiciona funcionalidade

fix(api): corrige erro

✨ feat(produto): adiciona cadastro

🐛 corrige bug

```



Motivos:



\* Falta Gitmoji

\* Falta tipo do commit

\* Falta escopo válido

\* Escopo não permitido

\* Mensagem genérica demais



\---



\## Tipos Permitidos



| Tipo       | Significado         | Quando usar                                                                        |

| ---------- | ------------------- | ---------------------------------------------------------------------------------- |

| `feat`     | Funcionalidade      | Quando adicionar uma nova funcionalidade                                           |

| `fix`      | Correção            | Quando corrigir um erro ou bug                                                     |

| `docs`     | Documentação        | Quando alterar documentação                                                        |

| `style`    | Estilo/Formatação   | Quando alterar formatação, layout ou organização visual sem mudar regra de negócio |

| `refactor` | Refatoração         | Quando melhorar o código sem alterar seu comportamento                             |

| `test`     | Testes              | Quando adicionar ou alterar testes                                                 |

| `chore`    | Tarefa geral        | Quando alterar configurações, scripts ou tarefas internas                          |

| `perf`     | Performance         | Quando melhorar desempenho                                                         |

| `build`    | Build               | Quando alterar empacotamento, dependências ou compilação                           |

| `ci`       | Integração contínua | Quando alterar pipelines e automações de CI/CD                                     |

| `revert`   | Reversão            | Quando reverter uma alteração anterior                                             |



\---



\## Gitmojis Permitidos



| Gitmoji | Uso sugerido                                   |

| ------- | ---------------------------------------------- |

| 🎉      | Início do projeto ou estrutura inicial         |

| ✨       | Nova funcionalidade                            |

| 🐛      | Correção de bug                                |

| ♻️      | Refatoração                                    |

| 📝      | Documentação                                   |

| 🎨      | Estilo, layout ou formatação                   |

| ✅       | Testes                                         |

| 🔧      | Configurações                                  |

| ⚡       | Performance                                    |

| 🚀      | Deploy, CI/CD ou publicação                    |

| 🔥      | Remoção de código ou arquivos                  |

| 🗃️     | Banco de dados                                 |

| 🔒      | Segurança                                      |

| ⬆️      | Atualização de dependências                    |

| 🚑      | Correção crítica                               |

| 🧾      | Comprovantes, relatórios ou documentos gerados |

| 📦      | Build, pacote ou artefato                      |

| 🐳      | Docker ou containers                           |

| 🔖      | Release, tag ou versão                         |

| ➕       | Adição de dependência                          |

| ➖       | Remoção de dependência                         |



\---



\# Glossário de Escopos



Os escopos ajudam a identificar a área do projeto afetada pelo commit.



Formato:



```bash

emoji tipo(escopo): descrição

```



Exemplo:



```bash

🔧 chore(config): ajusta configuração do projeto

```



\---



\## `project`



Representa o projeto como um todo.



Use quando a alteração afeta a estrutura geral do projeto ou não pertence a uma área específica.



Exemplos:



```bash

🎉 chore(project): adiciona estrutura inicial

♻️ refactor(project): reorganiza pastas principais

📝 docs(project): adiciona visão geral do projeto

```



Uso comum:



\* Estrutura inicial

\* Organização geral

\* Arquivos base

\* Primeiro commit do projeto



\---



\## `config`



Representa configurações do projeto ou de ferramentas.



Use quando alterar arquivos de configuração, ambiente, editor, formatador ou ferramentas auxiliares.



Exemplos:



```bash

🔧 chore(config): adiciona configuração do editor

🔧 chore(config): ajusta regras do linter

🎨 style(config): padroniza formatação automática

```



Arquivos comuns:



```bash

.editorconfig

.prettierrc

.eslintrc

settings.json

launch.json

appsettings.json

```



\---



\## `hooks`



Representa hooks do Git.



Use quando alterar scripts executados automaticamente pelo Git, como validações antes ou durante commits.



Exemplos:



```bash

🔧 chore(hooks): adiciona validação de commit-msg

🐛 fix(hooks): corrige regex de validação

♻️ refactor(hooks): simplifica hook de commit

```



Uso comum:



\* `commit-msg`

\* `pre-commit`

\* `pre-push`

\* Validação de mensagens de commit



\---



\## `git`



Representa configurações relacionadas ao Git e versionamento.



Use quando alterar arquivos ou configurações diretamente ligadas ao controle de versão.



Exemplos:



```bash

🔧 chore(git): adiciona arquivos ao gitignore

🔧 chore(git): configura gitattributes

🔧 chore(git): adiciona submodule de hooks

```



Arquivos comuns:



```bash

.gitignore

.gitattributes

.gitmodules

```



Diferença entre `git` e `hooks`:



\* `git`: configuração geral do versionamento

\* `hooks`: scripts executados pelo Git



\---



\## `docs`



Representa documentação.



Use quando alterar documentos, guias, instruções ou explicações do projeto.



Exemplos:



```bash

📝 docs(docs): atualiza documentação

📝 docs(docs): adiciona guia de instalação

📝 docs(docs): documenta padrão de commits

```



Arquivos comuns:



```bash

README.md

CONTRIBUTING.md

CHANGELOG.md

docs/

```



\---



\## `ci`



Representa integração contínua.



Use quando alterar pipelines, workflows e validações automáticas.



Exemplos:



```bash

🚀 ci(ci): adiciona workflow de validação

🐛 fix(ci): corrige execução dos testes no pipeline

🔧 chore(ci): configura GitHub Actions

```



Arquivos comuns:



```bash

.github/workflows/\*

.gitlab-ci.yml

azure-pipelines.yml

```



\---



\## `build`



Representa o processo de build, compilação ou empacotamento.



Use quando alterar algo relacionado à geração, compilação ou empacotamento do projeto.



Exemplos:



```bash

📦 build(build): ajusta script de empacotamento

🐛 fix(build): corrige erro na geração do artefato

🔧 chore(build): atualiza configuração de compilação

```



Arquivos comuns:



```bash

pom.xml

build.gradle

package.json

webpack.config.js

vite.config.js

```



\---



\## `deps`



Representa dependências do projeto.



Use quando adicionar, remover ou atualizar bibliotecas, pacotes, plugins ou dependências externas.



Exemplos:



```bash

⬆️ build(deps): atualiza dependências do projeto

➕ build(deps): adiciona biblioteca de validação

➖ build(deps): remove dependência não utilizada

```



Também é comum usar:



```bash

🔧 chore(deps): atualiza pacotes

```



\---



\## `release`



Representa versões e entregas.



Use quando preparar uma nova versão, criar changelog, tag ou ajustar informações de release.



Exemplos:



```bash

🔖 chore(release): prepara versão 1.0.0

📝 docs(release): atualiza changelog

🚀 build(release): gera pacote da versão 1.0.0

```



Arquivos comuns:



```bash

CHANGELOG.md

VERSION

package.json

pubspec.yaml

.csproj

```



\---



\## `tests`



Representa testes.



Use quando adicionar, corrigir ou reorganizar testes.



Exemplos:



```bash

✅ test(tests): adiciona testes de validação de commit

🐛 fix(tests): corrige cenário de teste quebrado

♻️ refactor(tests): reorganiza estrutura dos testes

```



Arquivos comuns:



```bash

\*.test.js

\*.spec.ts

Test\*.java

\*Tests.cs

```



\---



\## `core`



Representa o núcleo do sistema.



Use quando a alteração envolve regras principais, lógica central ou funcionalidades essenciais do projeto.



Exemplos:



```bash

✨ feat(core): adiciona regra principal de validação

🐛 fix(core): corrige fluxo base da aplicação

♻️ refactor(core): reorganiza lógica central

```



Uso comum:



\* Regras de negócio

\* Domínio da aplicação

\* Lógica principal

\* Fluxos essenciais



\---



\## `utils`



Representa utilitários e funções auxiliares.



Use quando alterar funções reutilizáveis, helpers, extensões ou métodos auxiliares.



Exemplos:



```bash

✨ feat(utils): adiciona função para normalizar texto

🐛 fix(utils): corrige formatação de data

♻️ refactor(utils): melhora helpers de validação

```



Pastas comuns:



```bash

utils/

helpers/

extensions/

common/

shared/

```



\---



\## `scripts`



Representa scripts auxiliares.



Use quando alterar scripts manuais, automações locais ou comandos de setup.



Exemplos:



```bash

🔧 chore(scripts): adiciona script de instalação dos hooks

🐛 fix(scripts): corrige execução no Windows

♻️ refactor(scripts): simplifica script de setup

```



Arquivos comuns:



```bash

setup-hooks.sh

setup-hooks.bat

install.sh

deploy.sh

```



Diferença entre `scripts` e `hooks`:



\* `hooks`: scripts executados automaticamente pelo Git

\* `scripts`: scripts auxiliares executados manualmente ou por automações



\---



\## `infra`



Representa infraestrutura.



Use quando alterar ambiente, containers, servidores, deploy ou configurações de infraestrutura.



Exemplos:



```bash

🐳 chore(infra): adiciona configuração Docker

🔧 chore(infra): configura ambiente de desenvolvimento

🚀 ci(infra): ajusta deploy automatizado

```



Arquivos comuns:



```bash

Dockerfile

docker-compose.yml

nginx.conf

terraform/

k8s/

```



\---



\## `security`



Representa segurança.



Use quando a alteração envolve permissões, autenticação, autorização, credenciais, tokens ou vulnerabilidades.



Exemplos:



```bash

🔒 fix(security): corrige exposição de credenciais

🔒 feat(security): adiciona validação de permissões

🔧 chore(security): atualiza política de secrets

```



Uso comum:



\* Permissões

\* Tokens

\* Secrets

\* Autenticação

\* Autorização

\* Criptografia

\* Vulnerabilidades



\---



\## `database`



Representa banco de dados.



Use quando alterar estrutura, migrations, seeds, consultas ou persistência de dados.



Exemplos:



```bash

🗃️ feat(database): adiciona migration de usuários

🐛 fix(database): corrige relacionamento entre tabelas

♻️ refactor(database): reorganiza queries de consulta

```



Arquivos e pastas comuns:



```bash

migrations/

seeds/

schema.sql

repositories/

dao/

```



\---



\## `ui`



Representa interface do usuário.



Use quando alterar telas, componentes visuais, layout, estilos ou responsividade.



Exemplos:



```bash

🎨 style(ui): ajusta espaçamento da tela inicial

✨ feat(ui): adiciona componente de menu lateral

🐛 fix(ui): corrige responsividade do formulário

```



Uso comum:



\* Telas

\* Componentes visuais

\* Layout

\* CSS

\* Responsividade

\* Ícones

\* Temas



\---



\## `api`



Representa APIs e integrações.



Use quando alterar endpoints, controllers, rotas, contratos, payloads ou chamadas externas.



Exemplos:



```bash

✨ feat(api): adiciona endpoint de autenticação

🐛 fix(api): corrige retorno de erro

♻️ refactor(api): reorganiza contratos de resposta

```



Uso comum:



\* Controllers

\* Routes

\* Endpoints

\* DTOs

\* Payloads

\* Requisições HTTP

\* Integrações externas



\---



\# Como instalar em um projeto



Este repositório pode ser usado como submodule dentro de outros projetos.



Na raiz do projeto que utilizará os hooks:



```bash

git submodule add https://github.com/seu-usuario/git-hooks.git .githooks

git config core.hooksPath .githooks

```



Depois, faça o commit da configuração:



```bash

git add .gitmodules .githooks

git commit -m "🔧 chore(config): adiciona hooks compartilhados"

```



\---



\# Como configurar após clonar um projeto



Ao clonar um projeto que usa este repositório como submodule:



```bash

git clone --recurse-submodules https://github.com/seu-usuario/seu-projeto.git

cd seu-projeto

git config core.hooksPath .githooks

```



Caso o projeto já tenha sido clonado sem os submodules:



```bash

git submodule update --init --recursive

git config core.hooksPath .githooks

```



\---



\# Como atualizar os hooks em um projeto



Dentro do projeto que utiliza os hooks:



```bash

cd .githooks

git pull origin main

cd ..

git add .githooks

git commit -m "🔧 chore(config): atualiza hooks compartilhados"

```



\---



\# Manutenção do Hook



O arquivo principal de validação é:



```bash

commit-msg

```



Nele são mantidos:



\* Gitmojis permitidos

\* Tipos permitidos

\* Escopos permitidos

\* Regex de validação

\* Mensagens de erro



Sempre que alterar o hook, recomenda-se executar os testes antes de publicar uma nova versão.



Exemplos de commits para manutenção:



```bash

🐛 fix(hooks): corrige regex de validação

✨ feat(hooks): adiciona novos escopos permitidos

🔧 chore(config): atualiza padrão de commits

📝 docs(docs): atualiza guia de utilização

✅ test(tests): adiciona casos de validação

```



\---



\# Sugestão de Primeiro Commit



Use:



```bash

🎉 chore(project): adiciona estrutura inicial

```



\---



\# Licença



Este projeto pode ser utilizado livremente para padronização de commits em projetos pessoais, acadêmicos ou profissionais.



