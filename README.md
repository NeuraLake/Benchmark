# NeuraLake API - Benchmark & Analytics Dashboard

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Version](https://img.shields.io/badge/version-1.0.0-emerald.svg)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.x-38bdf8.svg)
![Chart.js](https://img.shields.io/badge/Chart.js-4.x-ff6384.svg)

Um dashboard analítico estático de alta performance projetado para avaliar, auditar e simular cenários financeiros e de SLA bancário para a infraestrutura de modelos de linguagem da **NeuraLake Inference API**. O painel ajuda a validar a eficiência do algoritmo de roteamento inteligente (`auto`) comparado a modelos estáticos.

---

## 🚀 Funcionalidades Principais

*   **Abordagem Zero-Data Inicial**: O sistema inicia completamente zerado (KPIs, gráficos e tabelas limpos), aguardando estritamente o upload do arquivo de benchmark para evitar poluição visual ou dados falsos pré-carregados.
*   **Modo Claro & Escuro Nativo**: Interface adaptativa com alto contraste cirúrgico. Elementos críticos como o **Resumo Executivo** e as tabelas técnicas foram revisados para garantir legibilidade impecável independente do tema selecionado.
*   **Visualização Temporal Interativa**: Gráfico comparativo detalhando as frações de tempo de resposta:
    *   **TTFT** (*Time to First Token*)
    *   **TTFAT** (*Time to First Audible/Visible Token*) — essencial para a experiência do usuário final.
    *   **Tempo de Raciocínio** (*Thinking Time*) para modelos baseados em *Reasoning*.
*   **Gráfico Analítico Avançado**: Alternância dinâmica entre duas métricas cruciais:
    *   Consumo volumétrico de tokens (Entrada vs. Saída Visível vs. Raciocínio Oculto).
    *   Custo normalizado extrapolado por Milhão de Requisições.
*   **Filtros Granulares Multi-Nível**: Botões de filtragem rápida por cenário (Fácil, Comum, Difícil, Complexo) integrados diretamente no painel de simulação financeira e no relatório técnico detalhado (trabalhando em conjunto com a busca textual).
*   **Auditoria de Roteador Inteligente**: Mapeamento visual das decisões tomadas pela rota `auto`, sinalizando com tags de `Ideal` ou `Alerta` se o modelo escolhido condiz com a complexidade do prompt, além de projetar a economia real versus o uso fixo de modelos topo de linha (*Reasoning-Pro*).

---

## 🛠️ Tecnologias Utilizadas

O painel foi construído utilizando uma arquitetura *serverless* estática (Single HTML) para máxima portabilidade e agilidade:

*   **HTML5 & CSS3** (Customização de scrollbars e gradientes de fundo via propriedades CSS nativas).
*   **Tailwind CSS (v3.x)**: Framework utilitário configurado com injeção de classes de modo escuro dinâmico (`dark:`) e paleta de cores customizada (`brand`).
*   **Chart.js (v4.x)**: Renderização e gerenciamento dos estados dos gráficos de Latência, Distribuição de Custos e Métricas Avançadas.
*   **Lucide Icons**: Pacote de ícones vetoriais modernos e leves carregados dinamicamente via script.

---

## 📁 Estrutura de Arquivos

O projeto pode ser distribuído como um único arquivo ou integrado em uma estrutura web padrão:

```text
├── index.html                  # Arquivo único contendo a estrutura, estilos e lógica JS
└── README.md                   # Esta documentação do projeto
