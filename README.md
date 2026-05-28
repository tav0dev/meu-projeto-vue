# Projeto Landing Page - Deputado Estadual (Vue.js)

Este é o repositório do projeto de uma landing page interativa e responsiva desenvolvida para a campanha política fictícia (ou real) do "Deputado Estadual Rubem Gonzalez". O projeto foi construído utilizando as tecnologias mais modernas do ecossistema front-end.

## 🛠️ Tecnologias Utilizadas

- **Vue.js 3** (Composition API)
- **TypeScript**
- **Vite** (Build tool super rápida)
- **CSS3 Nativo** (Sem frameworks, utilizando CSS Variables, Flexbox, Grid e animações avançadas)

---

## 📋 Etapas de Desenvolvimento

Abaixo estão documentadas as etapas lógicas e cronológicas que guiaram a implementação deste projeto:

### 1. Configuração e Setup Inicial
- Criação do projeto base utilizando a ferramenta **Vite** com o template `vue-ts`.
- Limpeza dos arquivos padrão gerados pelo Vite para iniciar o desenvolvimento do zero.
- Configuração do `tsconfig.json` e definição do ambiente de desenvolvimento no `package.json`.

### 2. Estruturação Arquitetural e de Componentes
- Concentração do escopo principal no arquivo `App.vue` para uma estrutura do tipo Single Page Application (SPA).
- Divisão semântica do layout em seções estratégicas utilizando tags do HTML5 (`<nav>`, `<section>`, `<footer>`).
- Estruturação das seções principais:
  - **Navbar (Navegação)**
  - **Hero (Início)**
  - **Sobre**
  - **Bandeiras (Propostas)**
  - **Conquistas (Timeline)**
  - **Galeria e Depoimentos**
  - **Contato e Newsletter**

### 3. Implementação da Identidade Visual (Estilização)
- Criação de um design system básico via variáveis CSS nativas (`var(--verde-brasil)`, `var(--amarelo-brasil)`), seguindo a estética nacionalista proposta (verde, amarelo, azul e branco).
- Implementação de um tema imersivo com fundos escuros (`rgba(0, 10, 30)`), vidros foscos (`backdrop-filter: blur`) e gradientes modernos.
- Layout totalmente responsivo (Mobile First e Desktop) utilizando CSS Flexbox e Grid Layout.

### 4. Interatividade e Animações Avançadas (Vue + CSS)
- **Partículas Flutuantes:** Geração dinâmica de elementos visuais na seção Hero utilizando iteração do Vue (`v-for`) com propriedades de estilo aleatórias (tamanho e velocidade de animação).
- **Animações on Scroll:** Criação de diretivas e classes (`animate-on-scroll`, `scrolled`) que são ativadas a partir de event listeners globais acoplados no ciclo de vida do Vue (`onMounted`, `onUnmounted`).
- **Contadores Dinâmicos:** Lógica reativa com a Composition API (usando `reactive`) e `setInterval` para animar gradualmente as estatísticas ("Projetos de Lei", "Famílias Beneficiadas") na tela inicial.

### 5. Gestão de Estado e Formulários
- Implementação de formulários funcionais para **Contato** e **Newsletter**.
- Utilização de `v-model` para o *two-way data binding* dos campos de entrada.
- Tratamento de submissão (`@submit.prevent`) simulando o envio com feedbacks de sucesso (exibição reativa das mensagens de "Inscrição realizada" e "Mensagem enviada!").

### 6. Polimento Final e Ajustes Responsivos
- Implementação do botão "Voltar ao Topo", ativado baseando-se na posição do scroll (Y-axis).
- Criação de um menu *Mobile* interativo (Hamburger Menu) controlando o estado de abertura com classes CSS dinâmicas (ex: `:class="{ open: mobileOpen }"`).
- Testes e verificação no navegador (via `npm run dev`) para garantir a fluidez da landing page e a ausência de travamentos.

---

## 🚀 Como Rodar o Projeto Localmente

1. Certifique-se de ter o **Node.js** instalado na sua máquina.
2. Instale as dependências executando na raiz do projeto:
   ```bash
   npm install
   ```
3. Inicie o servidor de desenvolvimento:
   ```bash
   npm run dev
   ```
4. Acesse a URL gerada (geralmente `http://localhost:5173`) para visualizar e interagir com a aplicação.
