# Plano de Ação: Website Interativo - Núcleo de Estudos IA Generativa Aplicada ao Direito

Este documento delineia as próximas etapas e melhorias para o desenvolvimento do website interativo, abordando as *issues* levantadas no GitHub e incorporando novas ideias para enriquecer o conteúdo.

---

## I. Questões Fundamentais e Globais (Prioridade Alta)

- [ ] **Resolver Problema de Renderização do LaTeX (Issue #1)**  
  **Diagnóstico Final:**  
  - Verificar o console do navegador em múltiplas páginas (ex: `app1_explorador_pilares.html`) por erros específicos do KaTeX ou de carregamento de scripts CDN.  
  - Testar em diferentes navegadores (Chrome, Firefox, Opera) e limpar o cache agressivamente.  
  - Confirmar se os scripts `katex.min.js` e `auto-render.min.js` estão sendo carregados antes da tentativa de renderização.  

  **Tentativas de Solução (se o problema persistir):**  
  - Testar com uma configuração mínima do KaTeX em uma página de teste isolada.  
  - Verificar se há conflitos com outros scripts na página.  
  - Considerar carregar os scripts do KaTeX localmente (pasta `js/`) em vez de CDN.  
  - Como último recurso, avaliar gerar SVGs para as fórmulas principais.  

  **Aplicar Solução:**  
  - Implementar a correção em todas as páginas que utilizam LaTeX.

- [ ] **Implementar Estratégia de Navegação para Múltiplos Apps (Issue #2)**  
  **Design da Navegação:**  
  - Definir os 3-4 links principais visíveis.  
  - Criar menu dropdown "Mais Apps" para os demais links.  

  **Implementação HTML/CSS:**  
  - Atualizar `<nav class="app-navigation">` em todas as páginas.  
  - Adicionar CSS para dropdown.  

  **JavaScript (se necessário):**  
  - Implementar comportamento de clique no dropdown com acessibilidade.  

  **Responsividade:**  
  - Garantir funcionamento em dispositivos móveis (considerar menu hambúrguer).

- [ ] **Consistência e Refinamento do Tema Escuro/Claro**  
  **Revisão Global:**  
  - Verificar as 11 páginas e todos os elementos (textos, botões, tabelas, etc.).  

  **Fundo das Seções de Conteúdo:**  
  - Confirmar aplicação correta dos fundos `.content-section` e `.pillar-section-wrapper` em ambos os temas.  
  - Verificar variáveis CSS como `--gradient-content-1-dark`.  

  **Ícones:**  
  - Ajustar filtros CSS ou usar versões alternativas para boa visibilidade nos dois temas.

---

## II. Melhorias de Interatividade e Conteúdo (Prioridade Média)

- [ ] **Acesso às Fontes/Referências Citadas**  
  **Estratégia:**  
  - Opção 1: Página dedicada "Referências".  
  - Opção 2: Tooltips/contextuais por app.  
  - Opção 3: Seção "Referências" ao final de cada app.  

  **Implementação:**  
  - Adicionar conteúdo e links.

- [ ] **Interatividade e Visualização de Tabelas**  
  - App 2 (Hotspots Globais) & App 5 (Decodificador Dispositivos)  
  - Avaliar apresentação em cards/tabela  
  - Considerar filtros, ordenação, mini-gráficos radar, diagramas comparativos.

- [ ] **Uso de Acordeões ("Sanfona")**  
  - Revisar uso atual (App 1 e App 3)  
  - Avaliar utilidade em outros apps  
  - Refinar indicação de estado (ex: ícones de seta)

- [ ] **Geração de Prompts para Imagens e Gráficos Interativos (Conceitualização Inicial)**  
  **Identificar Oportunidades:**  
  - App 2: Mapa interativo  
  - App 9: Diagrama de rede  
  - Conceitos abstratos: imagens geradas por IA  

  **Definir Ferramentas/Abordagens:**  
  - Gráficos: Chart.js, D3.js, Recharts (em caso de migração para React)  
  - Imagens IA: Avaliar geração estática ou dinâmica  

  **Desenvolver Prompts Iniciais:**  
  - Esboçar exemplos para os casos acima

---

## III. Revisão e Refinamento por App (Trabalho Contínuo)

- [ ] **App 1:** Explorador dos Pilares (LaTeX e acordeão)  
- [ ] **App 2:** Hotspots Globais (cards/tabela)  
- [ ] **App 3:** Descomplicador de Barreiras (acordeão)  
- [ ] **App 4:** Casos Visão x Valores (clareza dos cards)  
- [ ] **App 5:** Decodificador Dispositivos (tabela)  
- [ ] **App 6:** Linguagem Natural (conteúdo/exemplos)  
- [ ] **App 7:** Balança Ética (conteúdo/exemplos)  
- [ ] **App 8:** Regulação vs. Inovação (conteúdo)  
- [ ] **App 9:** Teia da Transformação (visualização)  
- [ ] **App 10:** Dispositivos e Barreiras (conteúdo)  
- [ ] **App 11:** Paradoxo da Interação (conteúdo)

---

## IV. Documentação e Testes Finais

- [ ] **README.md:** Atualizar com descrição, instruções de uso e tecnologias.  
- [ ] **Testes Cross-Browser:** Chrome, Firefox, Opera, Edge, Safari.  
- [ ] **Testes de Responsividade:** Vários tamanhos de tela.  
- [ ] **Testes de Acessibilidade (Básico):** Contraste, navegação por teclado, `alt` nas imagens.

---

Este plano pode ser ajustado conforme avançamos. A ideia é ter um roteiro claro das tarefas pendentes e das melhorias desejadas.
