# InfluMax Copilot: Inteligência de Conteúdo com LLMs 🚀

> **Projeto Hands-On:** Estudo de Caso de Aplicações Práticas de LLMs  
> **Bootcamp:** Bradesco - Agentes de IA: Do Zero à Prática  
> **Plataforma:** [DIO (Digital Innovation One)](https://dio.me)

---

## 📌 1. Visão Geral do Projeto

A **InfluMax** é uma empresa de gestão e aceleração de criadores de conteúdo que precisava se reestruturar para voltar a crescer no mercado. 

Com o avanço da Inteligência Artificial, a empresa percebeu que criadores enfrentam três grandes desafios diários:
1. **Fadiga criativa / Bloqueio de ideias:** Dificuldade constante em ter ideias novas e originais.
2. **Perda de autenticidade:** Ao usar ferramentas genéricas de IA, o conteúdo gerado soa robótico, sem o tom de voz e a identidade do influenciador.
3. **Cópia vs. Inovação:** Muitos criadores apenas replicam o que já está em alta sem trazer um diferencial ou ângulo autoral.

O **InfluMax Copilot** é a solução proposta: um ecossistema inteligente baseado em Modelos de Linguagem de Larga Escala (LLMs) que atua como **mentor, pesquisador de tendências e diretor de gravação**, guiando o influenciador passo a passo, do planejamento à publicação.

---

## 💡 2. Como Funciona a Solução (Arquitetura em 3 Pilares)

```
┌──────────────────────────────────────┐     ┌───────────────────────────────────┐
│     Pilar 1: Onboarding Detalhado    │     │    Pilar 2: Pesquisa de Trends    │
│  (Perfil, Tom de Voz, Anti-Perfil)   │     │ (Temas em alta no nicho do autor) │
└──────────────────┬───────────────────┘     └─────────────────┬─────────────────┘
                   │                                           │
                   └─────────────────────┬─────────────────────┘
                                         ▼
                 ┌───────────────────────────────────────────────┐
                 │       LLM Contextualizada (System Prompt)     │
                 └───────────────────────┬───────────────────────┘
                                         ▼
                 ┌───────────────────────────────────────────────┐
                 │       Pilar 3: Chatbot & Diretor de Vídeo     │
                 │   - Validação da ideia inovadora              │
                 │   - Gancho (Hook) de retenção (0-3s)          │
                 │   - Roteiro estruturado com B-Roll            │
                 │   - Dicas práticas de gravação e ritmo        │
                 └───────────────────────────────────────────────┘
```

---

## 📋 3. Detalhamento dos Componentes

### 1. Onboarding Detalhado do Criador (Contexto Base)
A qualidade da resposta da IA depende da qualidade das informações fornecidas (*Garbage In, Garbage Out*). Na tela inicial, o criador é orientado:

> ⚠️ *"Quanto mais detalhes, nuances e verdades você compartilhar sobre o seu estilo e público, mais autêntica será a sua IA. Evite respostas de uma palavra!"*

Campos coletados:
* **Nicho e Subnicho:** Ex: *Finanças para jovens em início de carreira que ganham até 2 salários mínimos*.
* **Tom de Voz e Bordões:** Como fala, nível de informalidade, palavras habituais.
* **Anti-Perfil (O que NUNCA fazer):** Abordagens recusadas (ex: não falar de apostas, não fazer piadas ácidas, não usar termos excessivamente técnicos).
* **Métricas Atuais e Objetivos:** Situação de alcance atual e metas no curto prazo.
* **Referências e Inspirações:** Criadores que admira e o que especificamente admira neles (ritmo, didática, iluminação).
* **Links de Presença Digital:** Redes sociais em que atua ativamente.

---

### 2. Módulo de Busca de Tendências (Top Trends com Ângulo Inovador)
* A IA recebe as tendências atuais do nicho por meio de pesquisa integrada.
* Em vez de incentivar a cópia, o sistema identifica o padrão comum que todos estão fazendo e propõe um **ângulo autoral**, conectando a tendência às características únicas daquele influenciador.

---

### 3. Chatbot Mentor & Diretor de Vídeo (Execução Passo a Passo)
O chatbot não entrega apenas um texto pronto: ele divide a produção em etapas e orienta o influenciador:

1. **Etapa 1 - Ângulo Inovador:** Discute a oportunidade e sugere o enfoque do vídeo.
2. **Etapa 2 - Gancho (Hook - Primeiros 3 segundos):** Oferece opções com foco em prender a atenção e reter o público.
3. **Etapa 3 - Roteiro e Cenas:** Fala cronometrada acompanhada de indicação visual (o que mostrar na tela, gestos e cortes).
4. **Etapa 4 - Chamada para Ação (CTA):** Pergunta estratégica para gerar comentários e discussões reais.
5. **Etapa 5 - Direção de Gravação:** Instrução prática de postura, iluminação, tom de voz e ritmo da fala para a gravação.

---

## 🛠️ 4. Exemplo de Engenharia de Prompt (System Prompt)

```text
Você é o InfluMax Copilot, mentor estratégico de conteúdo e diretor de vídeos curtos da InfluMax.
Sua missão é instruir o criador a produzir conteúdos virais, inovadores e autênticos, baseando-se no perfil aprofundado dele e nas últimas tendências.

--- CONTEXTO DETALHADO DO CRIADOR ---
Nicho e Subnicho: {subnicho_detalhado}
Tom de voz e Bordões: {tom_e_bordoes}
O que NUNCA fazer (Anti-Perfil): {anti_perfil}
Objetivo Atual: {objetivo_metas}
Referências que admira: {referencias}

--- CONTEXTO DE TENDÊNCIAS (RESEARCH) ---
Tópico em Alta: {trend_identificada}
Padrão comum que todos estão fazendo: {padrao_repetitivo}

--- SUA METODOLOGIA DE ATUAÇÃO ---
1. Proponha um ângulo autoral para a tendência, evitando clichês e cópias.
2. Estruture o roteiro em passos:
   - Gancho (0 a 3s): Opções de impacto.
   - Desenvolvimento: Conteúdo direto (30 a 50s) com indicações de fala e ações de tela.
   - Fechamento (CTA): Pergunta magnética para gerar comentários.
3. Forneça uma dica prática de gravação (ritmo, tom, entonação ou iluminação).
```

---

## 📈 5. Impacto Esperado para a InfluMax

* **Escalabilidade:** Cada estrategista da InfluMax passa a atender mais criadores com apoio da IA.
* **Aumento de Engajamento:** Conteúdos com ganchos pensados e linguagem própria do criador geram maior retenção.
* **Diferenciação no Mercado:** Soluções que não se limitam a copiar tendências, gerando autoridade a longo prazo para os influenciadores.

---

## 👤 Autor

Desenvolvido por **Pedro Victor Alves Rodrigues Tavares** como parte do curso **Aplicações Práticas de LLMs** da trilha de IA da [DIO](https://dio.me).
