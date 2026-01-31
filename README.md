# VISION BOARD MZ

Plataforma digital de **orientação vocacional e planeamento de carreira** voltada para jovens moçambicanos, especialmente no período pós-9ª classe, ajudando-os a tomar decisões académicas e profissionais mais conscientes e alinhadas com seus interesses e habilidades.

---

## Visão Geral

Em Moçambique, muitos jovens escolhem cursos e carreiras sem orientação adequada, o que leva à frustração, abandono escolar e desperdício de talento.  
O **VISION BOARD MZ** nasce para resolver esse problema através de uma solução **digital, acessível e adaptada à realidade local**.

A plataforma oferece:
- Questionários de orientação vocacional
- Recomendações personalizadas de áreas de estudo
- Informação sobre cursos e instituições existentes em Moçambique
- Um plano visual simples com próximos passos de carreira

---

##  Estrutura do Monorepo

Este repositório segue uma arquitetura **monorepo**, organizando frontend, backend e documentação num único projeto.

```text
.
├── apps
│   ├── api
│   │   └── infra
│   └── web
│       ├── admin
│       └── site
├── doc
├── LICENSE
├── package.json
└── README.md
```
##  apps/api


Backend da aplicação.

Desenvolvido com Django + Django REST Framework

Responsável por:

Autenticação de usuários

Questionários vocacionais

Processamento e análise de respostas

Recomendações de áreas de estudo

APIs consumidas pelo frontend

##  apps/web

Frontend da aplicação.

site → Interface principal voltada para os jovens

admin → Painel administrativo (gestão de conteúdos, cursos, instituições, etc.)

Tecnologias frontend serão definidas e documentadas conforme a evolução do projeto.

##  doc

Documentação do projeto:

Ideias

Planeamento

Diagramas

Requisitos funcionais e não funcionais

##  Público-Alvo

Jovens que concluíram a 9ª classe

Estudantes do ensino secundário

Jovens indecisos quanto à carreira

Escolas e instituições de ensino (parceiros)

##  MVP (Produto Mínimo Viável)

A primeira versão do VISION BOARD MZ inclui:

Questionário online de interesses

Sistema básico de recomendações

Resultados personalizados

Interface simples e acessível via telemóvel

##  Tecnologias (Planeadas)
### Backend
- **Python**
- **Django**
- **Django REST Framework**
- API REST para comunicação com o frontend

### Frontend
- **TypeScript (TSX)**
- **Tailwind CSS** – estilização rápida e responsiva
- **GSAP** – animações avançadas
- **Framer Motion** – animações e transições modernas
- **Web responsiva**, otimizada para dispositivos móveis

### Inteligência & Automação
- **LangChain** – suporte a lógica inteligente para recomendações, fluxos de orientação e futuras integrações com IA

## Outros

Monorepo com Node.js (package.json)

Versionamento com Git

## Impacto Esperado

Redução de escolhas académicas inadequadas

Menor taxa de abandono escolar

Jovens mais conscientes e confiantes

Melhor alinhamento entre talento, formação e mercado de trabalho

## Contribuição

Contribuições são bem-vindas!
Este projeto tem um forte impacto social e educacional.
