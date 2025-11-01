# 🌍 Plataforma ONG — Sistema Web para Organizações Sociais

> **Projeto acadêmico criado por mim: Matheus Garcia, Universidade Cruzeiro do Sul, matéria de Desenvolvimento Front-End para Web**

> desenvolvido para permitir que ONGs gerenciem suas atividades, divulguem projetos, captem recursos e engajem voluntários em um ambiente web moderno, acessível e responsivo.

---

## 📋 Sumário
- [🎯 Objetivos](#-objetivos)
- [🌐 Visão Geral da Plataforma](#-visão-geral-da-plataforma)
- [👤 Personas e Casos de Uso](#-personas-e-casos-de-uso)
- [⚙️ Tecnologias Utilizadas](#️-tecnologias-utilizadas)
- [🧩 Arquitetura do Projeto](#-arquitetura-do-projeto)
- [🎨 Design System](#-design-system)
- [📱 Responsividade e Layout](#-responsividade-e-layout)
- [♿ Acessibilidade (WCAG 2.1 AA)](#-acessibilidade-wcag-21-aa)
- [🚀 Instalação e Execução Local](#-instalação-e-execução-local)
- [🔧 Estrutura de Pastas](#-estrutura-de-pastas)
- [💡 Metodologia de Desenvolvimento](#-metodologia-de-desenvolvimento)
- [🔀 Controle de Versão (GitFlow)](#-controle-de-versão-gitflow)
- [🤖 Integração Contínua e Releases](#-integração-contínua-e-releases)
- [🧪 Validação e Qualidade de Código](#-validação-e-qualidade-de-código)
- [🧱 Requisitos Técnicos Atendidos](#-requisitos-técnicos-atendidos)
- [📚 Licença](#-licença)

---

## 🎯 Objetivos

### **Objetivo Geral**
Desenvolver uma plataforma web completa e profissional que permita às ONGs gerenciar suas atividades, divulgar projetos, captar recursos e engajar voluntários.

### **Objetivos Específicos**
- Aplicar fundamentos de **HTML5**, **CSS3** e **JavaScript ES6+**.  
- Implementar **layouts responsivos** com **Flexbox** e **Grid**.  
- Criar **SPA básica** (Single Page Application) com manipulação de DOM.  
- Aplicar boas práticas de **acessibilidade** (WCAG 2.1 AA).  
- Utilizar **GitFlow** e **CI/CD** com **GitHub Actions**.  
- Entregar documentação técnica e código fonte padronizado.

---

## 🌐 Visão Geral da Plataforma

A **Plataforma ONG** oferece às organizações um portal institucional com:
- Área de **projetos sociais** (com indicadores e categorias).  
- Sistema de **voluntariado** (inscrições, histórico e certificados).  
- Módulo de **doações online** e **transparência financeira**.  
- Área pública para **divulgação, engajamento e notícias**.

---

## 👤 Personas e Casos de Uso

| Persona | Funções Principais |
|----------|--------------------|
| **Administrador da ONG** | Gerenciar informações, projetos, voluntários e doações. |
| **Voluntário** | Descobrir oportunidades, candidatar-se, acompanhar histórico. |
| **Doador** | Visualizar campanhas, realizar doações e acessar relatórios. |
| **Visitante** | Conhecer a ONG, visualizar projetos, acessar contatos. |

---

## ⚙️ Tecnologias Utilizadas

| Categoria | Ferramentas |
|------------|-------------|
| **Front-end** | HTML5, CSS3 (Grid/Flexbox), JavaScript ES6 |
| **Gestão de Versão** | Git + GitHub (GitFlow) |
| **Build & Otimização** | Terser, CSSO, HTML-Minifier, Imagemin |
| **CI/CD** | GitHub Actions + Semantic Release |
| **Acessibilidade** | Padrões WCAG 2.1 AA, ARIA, foco visível, teclado |
| **Documentação** | Markdown, templates automáticos (PR, Issues) |

---

## 🧩 Arquitetura do Projeto

```plaintext
plataforma-ong/
├── index.html
├── projetos.html
├── cadastro.html
├── css/
│   ├── styles.css
│   └── accessibility-themes.css
├── js/
│   ├── main.js
│   ├── spa-router.js
│   ├── validation.js
│   └── theme-toggle.js
├── assets/
│   ├── images/
│   └── icons/
├── .github/
│   ├── ISSUE_TEMPLATE/
│   ├── workflows/
│   └── PULL_REQUEST_TEMPLATE.md
├── .eslintrc.json
├── .prettierrc
├── package.json
└── README.md
🎨 Design System
O projeto utiliza um Design System modular e escalável com:

🎨 Paleta de cores (8 cores mínimas)
Tipo	Cores
Primárias	#11698E, #2FA6D6
Secundárias	#FDCB58, #F6A623
Neutras	#F7F7F8, #E0E0E0, #4A4A4A, #111111

🔤 Tipografia Hierárquica (5 níveis)
H1 — 32px

H2 — 24px

H3 — 20px

Body — 16px

Small/Texto auxiliar — 14px

📏 Sistema de espaçamento modular
8px, 16px, 24px, 32px, 48px, 64px

🧱 Componentes de Interface
Cards responsivos para projetos

Botões com estados (hover, focus, active, disabled)

Formulários com validação visual

Alerts, modais e toasts para feedback

Tags e badges para categorização

📱 Responsividade e Layout
Estrutura principal em CSS Grid (12 colunas)

Componentes internos com Flexbox

5 breakpoints responsivos:

320px, 480px, 768px, 1024px, 1280px

Layout mobile-first

Imagens otimizadas (webp, avif, lazy loading)

♿ Acessibilidade (WCAG 2.1 AA)
O projeto segue as diretrizes de acessibilidade digital, incluindo:

✅ Navegação completa por teclado
✅ Contraste mínimo de 4.5:1
✅ Estrutura semântica (landmarks ARIA)
✅ Skip link para o conteúdo principal
✅ Foco visível personalizado
✅ Modos dark e alto contraste

Exemplo:

html
Copiar código
<a class="skip-link" href="#main">Ir para o conteúdo principal</a>
🚀 Instalação e Execução Local
1️⃣ Pré-requisitos
Node.js ≥ 18

npm ≥ 9

2️⃣ Instalar dependências
bash
Copiar código
npm ci
3️⃣ Rodar localmente
bash
Copiar código
npm run start
4️⃣ Gerar build de produção
bash
Copiar código
npm run build
🔧 Estrutura de Pastas
plaintext
Copiar código
.github/           → workflows, templates, regras de contribuição
css/               → estilos globais e temas acessíveis
js/                → scripts modulares (SPA, validação, interatividade)
assets/images/     → imagens otimizadas
dist/              → saída de build minificada
💡 Metodologia de Desenvolvimento
O desenvolvimento segue princípios ágeis (Scrum/Kanban) com:

Sprints curtas e incrementais

Issues e milestones organizados no GitHub

Pull Requests com revisão de código

Versionamento semântico e changelog automático

🔀 Controle de Versão (GitFlow)
Branches principais

main → versão estável e liberada

develop → integração contínua

Branches auxiliares

feature/<nome> → novas funcionalidades

release/<versão> → preparação de release

hotfix/<correção> → correções urgentes

Exemplo de commit semântico:

yaml
Copiar código
feat: implementar formulário de cadastro com validação HTML5
fix: corrigir máscara de CPF em mobile
chore: configurar workflow de build no GitHub Actions
🤖 Integração Contínua e Releases
GitHub Actions configuradas:
CI (ci.yml): Lint, build, minificação e artifact automático

Release (release.yml): Semantic Release → gera tag e changelog

Semantic Release Plugins:
@semantic-release/changelog

@semantic-release/git

@semantic-release/github

🧪 Validação e Qualidade de Código
HTML5 validado via W3C Validator

ESLint e Prettier para padronização de código

Lighthouse / Axe para testes de acessibilidade

Tempo de carregamento < 5s (otimização de imagens e minificação)

🧱 Requisitos Técnicos Atendidos
Requisito	Implementado
Estrutura HTML5 semântica	✅
CSS modular com Design System	✅
Layout responsivo (Grid + Flex)	✅
SPA básica com manipulação DOM	✅
Validação de formulários com feedback	✅
Acessibilidade WCAG 2.1 AA	✅
GitFlow + Commits semânticos	✅
CI/CD (GitHub Actions + Releases)	✅
Minificação e compressão de imagens	✅
