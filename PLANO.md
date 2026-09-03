# PLANO DO PROJETO: Chat IA para Netlify (Campo Livre Standalone)

> Gerado automaticamente pelo SK Code Editor em 03/09/2026, 16:05:13
> **102 arquivo(s)** | **~20.404 linhas de codigo**

---

## RESUMO EXECUTIVO

- **Tipo de aplicacao:** Aplicacao Web Frontend (React)
- **Frontend / Stack principal:** React, TypeScript

**Para rodar o projeto:**
```bash
# Abra index.html no Preview (botao Play)
```

---

## ESTRUTURA DE ARQUIVOS

```
Chat IA para Netlify (Campo Livre Standalone)/
├── api-server-src/
│   ├── lib/
│   │   ├── devServerRegistry.ts
│   │   ├── logger.ts
│   │   ├── persistFiles.ts
│   │   └── storage.ts
│   ├── routes/
│   │   ├── ai.ts
│   │   ├── code-assistant.ts
│   │   ├── code-run.ts
│   │   ├── dev-server.ts
│   │   ├── exec.ts
│   │   ├── files.ts
│   │   ├── github.ts
│   │   ├── health.ts
│   │   ├── import-github.ts
│   │   ├── index.ts
│   │   ├── preview.ts
│   │   ├── projects.ts
│   │   ├── settings.ts
│   │   └── snippets.ts
│   ├── app.ts
│   └── index.ts
├── code-lens-src/
│   ├── components/
│   │   ├── ui/
│   │   │   ├── accordion.tsx
│   │   │   ├── alert-dialog.tsx
│   │   │   ├── alert.tsx
│   │   │   ├── aspect-ratio.tsx
│   │   │   ├── avatar.tsx
│   │   │   ├── badge.tsx
│   │   │   ├── breadcrumb.tsx
│   │   │   ├── button-group.tsx
│   │   │   ├── button.tsx
│   │   │   ├── calendar.tsx
│   │   │   ├── card.tsx
│   │   │   ├── carousel.tsx
│   │   │   ├── chart.tsx
│   │   │   ├── checkbox.tsx
│   │   │   ├── collapsible.tsx
│   │   │   ├── command.tsx
│   │   │   ├── context-menu.tsx
│   │   │   ├── dialog.tsx
│   │   │   ├── drawer.tsx
│   │   │   ├── dropdown-menu.tsx
│   │   │   ├── empty.tsx
│   │   │   ├── field.tsx
│   │   │   ├── form.tsx
│   │   │   ├── hover-card.tsx
│   │   │   ├── input-group.tsx
│   │   │   ├── input-otp.tsx
│   │   │   ├── input.tsx
│   │   │   ├── item.tsx
│   │   │   ├── kbd.tsx
│   │   │   ├── label.tsx
│   │   │   ├── menubar.tsx
│   │   │   ├── navigation-menu.tsx
│   │   │   ├── pagination.tsx
│   │   │   ├── popover.tsx
│   │   │   ├── progress.tsx
│   │   │   ├── radio-group.tsx
│   │   │   ├── resizable.tsx
│   │   │   ├── scroll-area.tsx
│   │   │   ├── select.tsx
│   │   │   ├── separator.tsx
│   │   │   ├── sheet.tsx
│   │   │   ├── sidebar.tsx
│   │   │   ├── skeleton.tsx
│   │   │   ├── slider.tsx
│   │   │   ├── sonner.tsx
│   │   │   ├── spinner.tsx
│   │   │   ├── switch.tsx
│   │   │   ├── table.tsx
│   │   │   ├── tabs.tsx
│   │   │   ├── textarea.tsx
│   │   │   ├── toast.tsx
│   │   │   ├── toaster.tsx
│   │   │   ├── toggle-group.tsx
│   │   │   ├── toggle.tsx
│   │   │   └── tooltip.tsx
│   │   ├── ai-panel.tsx
│   │   ├── code-editor.tsx
│   │   ├── code-viewer.tsx
│   │   ├── error-boundary.tsx
│   │   ├── file-tree.tsx
│   │   ├── github-deploy-modal.tsx
│   │   ├── layout.tsx
│   │   ├── packages-panel.tsx
│   │   ├── preview-panel.tsx
│   │   ├── terminal-panel.tsx
│   │   └── theme-provider.tsx
│   ├── hooks/
│   │   ├── use-file-ops.ts
│   │   ├── use-mobile.tsx
│   │   └── use-toast.ts
│   ├── lib/
│   │   └── utils.ts
│   ├── pages/
│   │   ├── assistant.tsx
│   │   ├── home.tsx
│   │   ├── not-found.tsx
│   │   ├── playground.tsx
│   │   ├── project-explorer.tsx
│   │   └── settings.tsx
│   ├── reference/
│   │   ├── code-assistant.tsx
│   │   └── playground.tsx
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
└── index.html
```

---

## STACK TECNOLOGICO DETECTADO

- **Frontend:** React, TypeScript

---

## ROTAS DA API (endpoints detectados automaticamente)

```
USE    /api  (em api-server-src/app.ts)
POST   /ai/chat  (em api-server-src/routes/ai.ts)
POST   /ai/analyze-file  (em api-server-src/routes/ai.ts)
POST   /ai/analyze-folder  (em api-server-src/routes/ai.ts)
POST   /ai/tts  (em api-server-src/routes/ai.ts)
POST   /code-assistant  (em api-server-src/routes/code-assistant.ts)
POST   /code/run  (em api-server-src/routes/code-run.ts)
POST   /projects/:projectId/dev-server/start  (em api-server-src/routes/dev-server.ts)
DELETE /projects/:projectId/dev-server/stop  (em api-server-src/routes/dev-server.ts)
GET    /projects/:projectId/dev-server/status  (em api-server-src/routes/dev-server.ts)
POST   /projects/:projectId/exec-stream  (em api-server-src/routes/exec.ts)
POST   /projects/:projectId/exec  (em api-server-src/routes/exec.ts)
GET    /projects/:projectId/files  (em api-server-src/routes/files.ts)
PUT    /projects/:projectId/files  (em api-server-src/routes/files.ts)
DELETE /projects/:projectId/files  (em api-server-src/routes/files.ts)
POST   /projects/:projectId/files/mkdir  (em api-server-src/routes/files.ts)
PATCH  /projects/:projectId/files  (em api-server-src/routes/files.ts)
POST   /projects/:projectId/files/copy  (em api-server-src/routes/files.ts)
POST   /github/create-repo  (em api-server-src/routes/github.ts)
GET    /healthz  (em api-server-src/routes/health.ts)
POST   /projects/import-github  (em api-server-src/routes/import-github.ts)
GET    /projects/:projectId/preview/status  (em api-server-src/routes/preview.ts)
GET    /projects/:projectId/preview/*path  (em api-server-src/routes/preview.ts)
GET    /projects  (em api-server-src/routes/projects.ts)
POST   /projects  (em api-server-src/routes/projects.ts)
GET    /api/hello  (em api-server-src/routes/projects.ts)
POST   /projects/blank  (em api-server-src/routes/projects.ts)
GET    /projects/:projectId  (em api-server-src/routes/projects.ts)
GET    /projects/:projectId/download  (em api-server-src/routes/projects.ts)
DELETE /projects/:projectId  (em api-server-src/routes/projects.ts)
GET    /settings  (em api-server-src/routes/settings.ts)
PUT    /settings  (em api-server-src/routes/settings.ts)
GET    /snippets  (em api-server-src/routes/snippets.ts)
POST   /snippets  (em api-server-src/routes/snippets.ts)
PATCH  /snippets/:id  (em api-server-src/routes/snippets.ts)
DELETE /snippets/:id  (em api-server-src/routes/snippets.ts)
```

---

## VARIAVEIS DE AMBIENTE NECESSARIAS

Crie um arquivo `.env` na raiz com estas variaveis:

```env
LOG_LEVEL=seu_valor_aqui
STORAGE_PATH=seu_valor_aqui
AI_INTEGRATIONS_GEMINI_BASE_URL=seu_valor_aqui
AI_INTEGRATIONS_GEMINI_API_KEY=seu_valor_aqui
PATH=seu_valor_aqui
PORT=seu_valor_aqui
```

---

## ARQUIVOS PRINCIPAIS

- `api-server-src/app.ts` — Ponto de entrada do backend
- `api-server-src/index.ts` — Ponto de entrada do backend
- `api-server-src/routes/index.ts` — Ponto de entrada do backend
- `code-lens-src/App.tsx` — Componente raiz do frontend
- `code-lens-src/main.tsx` — Arquivo principal
- `index.html` — Pagina HTML principal

---

## GUIA COMPLETO — O QUE CADA PARTE DO PROJETO FAZ

> Esta secao explica, em linguagem simples, o que e para que serve cada pasta e cada arquivo.

### 📁 Raiz do Projeto (pasta principal)
> Arquivos de configuracao e pontos de entrada ficam aqui.

**`index.html`** _(25 linhas)_
Pagina HTML raiz do projeto. E o ponto de entrada que o browser carrega primeiro.

---

### 📁 `api-server-src/`
> Pasta 'api-server-src' — agrupamento de arquivos relacionados.

**`app.ts`** _(56 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`index.ts`** _(26 linhas)_
Arquivo INDEX — ponto de entrada da pasta, exporta tudo que esta dentro.

---

### 📁 `code-lens-src/`
> Pasta 'code-lens-src' — agrupamento de arquivos relacionados.

**`App.tsx`** _(43 linhas)_
Componente RAIZ do frontend — e o pai de todos os outros componentes. Aqui ficam as rotas principais.

**`index.css`** _(386 linhas)_
Arquivo de estilos visuais — cores, tamanhos, fontes, espacamentos da interface.

**`main.tsx`** _(12 linhas)_
Ponto de entrada do React — monta o componente App na pagina HTML.

---

### 📁 `api-server-src/lib/`
> Funcoes auxiliares reutilizaveis em varios lugares do projeto.

**`devServerRegistry.ts`** _(345 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`logger.ts`** _(21 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`persistFiles.ts`** _(143 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`storage.ts`** _(161 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

---

### 📁 `api-server-src/routes/`
> Definicao das URLs e navegacao do app.

**`ai.ts`** _(712 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`code-assistant.ts`** _(162 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`code-run.ts`** _(47 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`dev-server.ts`** _(231 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`exec.ts`** _(354 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`files.ts`** _(184 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`github.ts`** _(171 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`health.ts`** _(12 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`import-github.ts`** _(169 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`index.ts`** _(33 linhas)_
Arquivo INDEX — ponto de entrada da pasta, exporta tudo que esta dentro.

**`preview.ts`** _(141 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`projects.ts`** _(521 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`settings.ts`** _(78 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

**`snippets.ts`** _(67 linhas)_
Arquivo TypeScript/JavaScript — logica, funcoes ou modulo do projeto.

---

### 📁 `code-lens-src/components/`
> Pecas visuais reutilizaveis da interface (botoes, cards, formularios...).

**`ai-panel.tsx`** _(1177 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`code-editor.tsx`** _(241 linhas)_
Componente EDITOR — area de edicao de texto, codigo ou conteudo rico.

**`code-viewer.tsx`** _(302 linhas)_
Componente de PAGINA/TELA — representa uma tela completa navegavel no app.

**`error-boundary.tsx`** _(107 linhas)_
Componente de ERRO — exibido quando algo da errado, com mensagem explicativa.

**`file-tree.tsx`** _(389 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`github-deploy-modal.tsx`** _(626 linhas)_
Componente MODAL — janela/popup que aparece sobre a tela pedindo uma acao ou mostrando uma informacao importante.

**`layout.tsx`** _(160 linhas)_
Componente de LAYOUT — define a estrutura visual da pagina (cabecalho, sidebar, rodape). Envolve outros componentes.

**`packages-panel.tsx`** _(537 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`preview-panel.tsx`** _(586 linhas)_
Componente de PAGINA/TELA — representa uma tela completa navegavel no app.

**`terminal-panel.tsx`** _(555 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`theme-provider.tsx`** _(72 linhas)_
Componente PROVIDER — 'fornece' dados/funcoes para todos os componentes filhos via Context API do React.

---

### 📁 `code-lens-src/hooks/`
> Hooks React customizados — logica reutilizavel de estado e efeitos.

**`use-file-ops.ts`** _(110 linhas)_
HOOK React personalizado para gerenciar estado/comportamento de '-file-ops'.

**`use-mobile.tsx`** _(22 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`use-toast.ts`** _(188 linhas)_
HOOK React personalizado para gerenciar estado/comportamento de '-toast'.

---

### 📁 `code-lens-src/lib/`
> Funcoes auxiliares reutilizaveis em varios lugares do projeto.

**`utils.ts`** _(16 linhas)_
Funcoes UTILITARIAS — ferramentas reutilizaveis de uso geral no projeto.

---

### 📁 `code-lens-src/pages/`
> Telas completas do app — cada arquivo aqui e uma pagina navegavel.

**`assistant.tsx`** _(514 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`home.tsx`** _(663 linhas)_
Componente HOME — pagina/tela inicial do app.

**`not-found.tsx`** _(22 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`playground.tsx`** _(666 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`project-explorer.tsx`** _(681 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`settings.tsx`** _(666 linhas)_
Componente de CONFIGURACOES — tela onde o usuario ajusta preferencias do app.

---

### 📁 `code-lens-src/reference/`
> Pasta 'reference' — agrupamento de arquivos relacionados.

**`code-assistant.tsx`** _(749 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`playground.tsx`** _(1473 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

---

### 📁 `code-lens-src/components/ui/`
> Componentes de UI (interface) basicos e genericos.

**`accordion.tsx`** _(55 linhas)_
Componente ACCORDION — secoes que abrem/fecham ao clicar, economizando espaco na tela.

**`alert-dialog.tsx`** _(139 linhas)_
Componente de NOTIFICACAO/ALERTA — mensagem temporaria que aparece na tela (ex: 'Salvo com sucesso!').

**`alert.tsx`** _(59 linhas)_
Componente de NOTIFICACAO/ALERTA — mensagem temporaria que aparece na tela (ex: 'Salvo com sucesso!').

**`aspect-ratio.tsx`** _(6 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`avatar.tsx`** _(50 linhas)_
Componente AVATAR — foto ou iniciais do usuario em formato circular.

**`badge.tsx`** _(43 linhas)_
Componente BADGE (etiqueta) — pequeno indicador com numero ou status (ex: '3 novas mensagens').

**`breadcrumb.tsx`** _(115 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`button-group.tsx`** _(83 linhas)_
Componente de BOTAO — elemento clicavel reutilizavel com estilo padrao do projeto.

**`button.tsx`** _(65 linhas)_
Componente de BOTAO — elemento clicavel reutilizavel com estilo padrao do projeto.

**`calendar.tsx`** _(213 linhas)_
Componente CALENDARIO/AGENDA — visualizacao e selecao de datas e eventos.

**`card.tsx`** _(83 linhas)_
Componente CARD (cartao) — exibe uma informacao em um bloco visual com borda e sombra. Muito usado para listas de items.

**`carousel.tsx`** _(260 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`chart.tsx`** _(367 linhas)_
Componente de GRAFICO — visualizacao de dados em forma de grafico (barras, linhas, pizza...).

**`checkbox.tsx`** _(28 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`collapsible.tsx`** _(12 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`command.tsx`** _(153 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`context-menu.tsx`** _(198 linhas)_
CONTEXT do React — mecanismo para compartilhar dados entre componentes sem passar por props.

**`dialog.tsx`** _(120 linhas)_
Componente DIALOG — caixa de dialogo que exige resposta do usuario (confirmar, cancelar...).

**`drawer.tsx`** _(116 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`dropdown-menu.tsx`** _(201 linhas)_
Componente de MENU/DROPDOWN — lista de opcoes que aparece ao clicar em um botao.

**`empty.tsx`** _(104 linhas)_
Componente de ESTADO VAZIO — exibido quando nao ha dados para mostrar (ex: 'Nenhum resultado encontrado').

**`field.tsx`** _(244 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`form.tsx`** _(179 linhas)_
Componente de FORMULARIO — campos de entrada de dados (texto, selecao, etc.) com validacao.

**`hover-card.tsx`** _(27 linhas)_
Componente CARD (cartao) — exibe uma informacao em um bloco visual com borda e sombra. Muito usado para listas de items.

**`input-group.tsx`** _(168 linhas)_
Componente de CAMPO DE ENTRADA — elemento de input com estilo personalizado.

**`input-otp.tsx`** _(69 linhas)_
Componente de CAMPO DE ENTRADA — elemento de input com estilo personalizado.

**`input.tsx`** _(22 linhas)_
Componente de CAMPO DE ENTRADA — elemento de input com estilo personalizado.

**`item.tsx`** _(193 linhas)_
Componente de ITEM — representa um elemento individual dentro de uma lista ou colecao.

**`kbd.tsx`** _(29 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`label.tsx`** _(26 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`menubar.tsx`** _(254 linhas)_
Componente de MENU/DROPDOWN — lista de opcoes que aparece ao clicar em um botao.

**`navigation-menu.tsx`** _(128 linhas)_
Componente de NAVEGACAO/CABECALHO — barra superior com logo, menu e links de navegacao.

**`pagination.tsx`** _(117 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`popover.tsx`** _(31 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`progress.tsx`** _(28 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`radio-group.tsx`** _(42 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`resizable.tsx`** _(45 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`scroll-area.tsx`** _(46 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`select.tsx`** _(159 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`separator.tsx`** _(29 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`sheet.tsx`** _(140 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`sidebar.tsx`** _(727 linhas)_
Componente de BARRA LATERAL — menu ou painel que aparece na lateral da tela.

**`skeleton.tsx`** _(16 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`slider.tsx`** _(26 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`sonner.tsx`** _(32 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`spinner.tsx`** _(16 linhas)_
Componente de CARREGAMENTO — animacao visual que aparece enquanto dados estao sendo buscados.

**`switch.tsx`** _(27 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`table.tsx`** _(120 linhas)_
Componente de TABELA — exibe dados em linhas e colunas.

**`tabs.tsx`** _(53 linhas)_
Componente de ABAS — permite alternar entre diferentes secoes de conteudo com clique.

**`textarea.tsx`** _(22 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`toast.tsx`** _(127 linhas)_
Componente de NOTIFICACAO/ALERTA — mensagem temporaria que aparece na tela (ex: 'Salvo com sucesso!').

**`toaster.tsx`** _(34 linhas)_
Componente de NOTIFICACAO/ALERTA — mensagem temporaria que aparece na tela (ex: 'Salvo com sucesso!').

**`toggle-group.tsx`** _(61 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`toggle.tsx`** _(43 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

**`tooltip.tsx`** _(32 linhas)_
Componente React — parte visual reutilizavel da interface do usuario.

---

## CONTEXTO PARA IA (copie e cole para continuar o projeto)

> Use este bloco para explicar o projeto para qualquer IA ou desenvolvedor:

```
Projeto: Chat IA para Netlify (Campo Livre Standalone)
Tipo: Aplicacao Web Frontend (React)
Stack: React, TypeScript
Arquivos: 102 | Linhas: ~20.404
Rotas API: 36 endpoint(s) detectado(s)
Variaveis de ambiente necessarias: LOG_LEVEL, STORAGE_PATH, AI_INTEGRATIONS_GEMINI_BASE_URL, AI_INTEGRATIONS_GEMINI_API_KEY, PATH, PORT

Estrutura principal:
  api-server-src/app.ts
  api-server-src/index.ts
  api-server-src/lib/devServerRegistry.ts
  api-server-src/lib/logger.ts
  api-server-src/lib/persistFiles.ts
  api-server-src/lib/storage.ts
  api-server-src/routes/ai.ts
  api-server-src/routes/code-assistant.ts
  api-server-src/routes/code-run.ts
  api-server-src/routes/dev-server.ts
  api-server-src/routes/exec.ts
  api-server-src/routes/files.ts
  api-server-src/routes/github.ts
  api-server-src/routes/health.ts
  api-server-src/routes/import-github.ts
  api-server-src/routes/index.ts
  api-server-src/routes/preview.ts
  api-server-src/routes/projects.ts
  api-server-src/routes/settings.ts
  api-server-src/routes/snippets.ts
  code-lens-src/App.tsx
  code-lens-src/components/ai-panel.tsx
  code-lens-src/components/code-editor.tsx
  code-lens-src/components/code-viewer.tsx
  code-lens-src/components/error-boundary.tsx
  code-lens-src/components/file-tree.tsx
  code-lens-src/components/github-deploy-modal.tsx
  code-lens-src/components/layout.tsx
  code-lens-src/components/packages-panel.tsx
  code-lens-src/components/preview-panel.tsx
  code-lens-src/components/terminal-panel.tsx
  code-lens-src/components/theme-provider.tsx
  code-lens-src/components/ui/accordion.tsx
  code-lens-src/components/ui/alert-dialog.tsx
  code-lens-src/components/ui/alert.tsx
  code-lens-src/components/ui/aspect-ratio.tsx
  code-lens-src/components/ui/avatar.tsx
  code-lens-src/components/ui/badge.tsx
  code-lens-src/components/ui/breadcrumb.tsx
  code-lens-src/components/ui/button-group.tsx
  code-lens-src/components/ui/button.tsx
  code-lens-src/components/ui/calendar.tsx
  code-lens-src/components/ui/card.tsx
  code-lens-src/components/ui/carousel.tsx
  code-lens-src/components/ui/chart.tsx
  code-lens-src/components/ui/checkbox.tsx
  code-lens-src/components/ui/collapsible.tsx
  code-lens-src/components/ui/command.tsx
  code-lens-src/components/ui/context-menu.tsx
  code-lens-src/components/ui/dialog.tsx
  code-lens-src/components/ui/drawer.tsx
  code-lens-src/components/ui/dropdown-menu.tsx
  code-lens-src/components/ui/empty.tsx
  code-lens-src/components/ui/field.tsx
  code-lens-src/components/ui/form.tsx
  code-lens-src/components/ui/hover-card.tsx
  code-lens-src/components/ui/input-group.tsx
  code-lens-src/components/ui/input-otp.tsx
  code-lens-src/components/ui/input.tsx
  code-lens-src/components/ui/item.tsx
  code-lens-src/components/ui/kbd.tsx
  code-lens-src/components/ui/label.tsx
  code-lens-src/components/ui/menubar.tsx
  code-lens-src/components/ui/navigation-menu.tsx
  code-lens-src/components/ui/pagination.tsx
  code-lens-src/components/ui/popover.tsx
  code-lens-src/components/ui/progress.tsx
  code-lens-src/components/ui/radio-group.tsx
  code-lens-src/components/ui/resizable.tsx
  code-lens-src/components/ui/scroll-area.tsx
  code-lens-src/components/ui/select.tsx
  code-lens-src/components/ui/separator.tsx
  code-lens-src/components/ui/sheet.tsx
  code-lens-src/components/ui/sidebar.tsx
  code-lens-src/components/ui/skeleton.tsx
  code-lens-src/components/ui/slider.tsx
  code-lens-src/components/ui/sonner.tsx
  code-lens-src/components/ui/spinner.tsx
  code-lens-src/components/ui/switch.tsx
  code-lens-src/components/ui/table.tsx
  code-lens-src/components/ui/tabs.tsx
  code-lens-src/components/ui/textarea.tsx
  code-lens-src/components/ui/toast.tsx
  code-lens-src/components/ui/toaster.tsx
  code-lens-src/components/ui/toggle-group.tsx
  code-lens-src/components/ui/toggle.tsx
  code-lens-src/components/ui/tooltip.tsx
  code-lens-src/hooks/use-file-ops.ts
  code-lens-src/hooks/use-mobile.tsx
  code-lens-src/hooks/use-toast.ts
  code-lens-src/index.css
  code-lens-src/lib/utils.ts
  code-lens-src/main.tsx
  code-lens-src/pages/assistant.tsx
  code-lens-src/pages/home.tsx
  code-lens-src/pages/not-found.tsx
  code-lens-src/pages/playground.tsx
  code-lens-src/pages/project-explorer.tsx
  code-lens-src/pages/settings.tsx
  code-lens-src/reference/code-assistant.tsx
  code-lens-src/reference/playground.tsx
  index.html
```

---

*Plano gerado pelo SK Code Editor — 03/09/2026, 16:05:13*