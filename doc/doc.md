# Casos de Uso – VISION BOARD MZ

Este documento organiza os casos de uso da plataforma **VISION BOARD MZ** em categorias **Primários** e **Secundários**, considerando usuários **anonimizados** ou logados, e administradores/escolas.

---

##  Casos de Uso Primários (Funções Centrais)

### Usuário Jovem (anonimamente ou logado)

| Categoria | Caso de Uso | Descrição | Observações |
|-----------|------------|-----------|------------|
| Geral | Preencher Questionário | Responder perguntas sobre interesses, habilidades e preferências | Pode ser anônimo |
| Geral | Receber Recomendações | Obter áreas de estudo e carreiras sugeridas | Processamento via regras ou LangChain |
| Geral | Visualizar Plano de Futuro | Visualizar mapa visual com próximos passos (curso, escola, metas) | Anônimo ou logado |
| Geral | Gerar PDF | Criar e baixar PDF do plano de carreira | Disponível para todos |
| Específico | Criar Conta (opcional) | Salvar progresso, histórico e planos futuros | Só para quem deseja |

---

### Administrador / Escola

| Categoria | Caso de Uso | Descrição | Observações |
|-----------|------------|-----------|------------|
| Geral | Gerenciar Cursos e Instituições | Adicionar, editar ou remover cursos e escolas | Controle total do conteúdo |
| Geral | Gerenciar Questionários | Criar ou atualizar perguntas do questionário vocacional | Pode ativar/desativar perguntas |
| Geral | Analisar Resultados | Relatórios de uso e respostas agregadas | Sem expor dados pessoais de anônimos |
| Específico | Gerenciar Usuários | Criar, editar ou desativar contas | Apenas para contas logadas |

---

##  Casos de Uso Secundários (Funções Complementares)

### Usuário Jovem

| Categoria | Caso de Uso | Descrição | Observações |
|-----------|------------|-----------|------------|
| Secundário | Compartilhar PDF | Permitir compartilhar plano via link ou email | Opcional, sem salvar dados no servidor |
| Secundário | Customizar Plano | Escolher cores, ícones ou metas visuais | Melhor experiência visual |
| Secundário | Feedback | Enviar feedback sobre recomendações | Coleta anônima ou logada |

### Administrador / Escola

| Categoria | Caso de Uso | Descrição | Observações |
|-----------|------------|-----------|------------|
| Secundário | Monitorar Atividade | Ver número de questionários respondidos e PDFs gerados | Métricas agregadas, anonimizadas |
| Secundário | Configurar Sistema | Ajustar limites, temporizadores ou regras de recomendação | Mantém flexibilidade do sistema |

---

##  Resumo – Primários vs Secundários

| Tipo | Funções |
|------|---------|
| Primários | Preencher questionário, receber recomendações, visualizar plano, gerar PDF, gerenciar conteúdo (admin) |
| Secundários | Compartilhar PDF, customizar plano, feedback, monitorar atividades, configurações adicionais |



```text
Usuário (anônimo)
      │
      ▼
Preenche Questionário
      │
      ▼
Backend (Django REST Framework)
  - Processa respostas
  - Gera recomendações (LangChain / regras)
      │
      ▼
Frontend (TSX + Tailwind + GSAP/Framer)
  - Mostra recomendações personalizadas
  - Visualiza plano de carreira
  - Botão "Gerar PDF" → PDF gerado e baixado
```


```text
Usuário (logado) [opcional]
      │
      ▼
Mesma lógica do anônimo
      │
      ▼
Mas respostas e histórico são salvos no banco

```