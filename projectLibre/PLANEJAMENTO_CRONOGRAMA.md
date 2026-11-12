# Planejamento do Projeto - ProjectLibre (EAP e Cronograma)

Este documento reflete a estrutura exata montada no **ProjectLibre** com a tarefa-raiz **TCC**, as fases indentadas e as sub-tarefas com durações em dias, cobrindo o período de **29/06** a **04/12**.

---

## 👥 Recursos Envolvidos (Equipe)

- **Daniel Douglas Melo Gomes Neto** (Trabalho / *Work*)
- **José Carlos Vaz Felipe** (Trabalho / *Work*)
- **Lucas Alves Dos Reis** (Trabalho / *Work*)
- **Pedro Henrique Pereira Medeiros Spíndola** (Trabalho / *Work*)
- **Orientação:** Profª. Ramyres Aquino (Reuniões semanais às quintas-feiras)

---

## 📅 Marcos Principais do Calendário

- **29/06:** Início do projeto e organização do repositório no GitHub.
- **04/09:** Entrega formal do Plano de Pesquisa.
- **07/10:** Recebimento do Modelo oficial de Monografia.
- **27/10:** Entrega da 1ª versão funcional do simulador Mock.
- **04/12:** **Entrega Final de todo o TCC e Fábrica de Software.**

---

## 📊 Estrutura Hierárquica de Tarefas para o ProjectLibre

> **Regra importante sobre Antecessores no ProjectLibre:**
> - O número na coluna **Antecessores** deve ser **exatamente o número da Linha (ID)** da tarefa anterior.
> - **Nunca** aponte para uma linha de fase de resumo/mãe (ex: linhas 1, 2, 5, 9, 13, 19, 23). Aponte sempre para a **tarefa operacional (folha)** que foi concluída.
> - Tarefas com **0 dias** viram marcos (*milestones* - losangos no gráfico).

| Linha (ID) | Nome | Duração | Início | Antecessores | Descrição |
| :---: | :--- | :---: | :---: | :---: | :--- |
| **1** | **TCC** | 115 dias | 29/06 | - | *Projeto Integrador TCC e Fábrica de Software* |
| **2** | &nbsp;&nbsp;**1. Iniciação e Autorização** | 3 dias | 29/06 | - | *Fase de abertura e validação com a indústria* |
| 3 | &nbsp;&nbsp;&nbsp;&nbsp;1.1 Criação e organização do repositório no GitHub | 1 dia | 29/06 | - | Setup de versionamento e governança do código |
| 4 | &nbsp;&nbsp;&nbsp;&nbsp;1.2 Reunião de alinhamento com a chefia da fábrica | 2 dias | 30/06 | **3** | Apresentação da ideia e autorização para o estudo |
| **5** | &nbsp;&nbsp;**2. Planejamento e Pesquisa** | 45 dias | 02/07 | - | *Fase de pesquisa teórica e plano inicial* |
| 6 | &nbsp;&nbsp;&nbsp;&nbsp;2.1 Pesquisa inicial e levantamento de referências (VIM, ISO) | 25 dias | 02/07 | **4** | Mapeamento dos requisitos normativos e metrológicos |
| 7 | &nbsp;&nbsp;&nbsp;&nbsp;2.2 Elaboração do documento de Plano de Pesquisa | 20 dias | 05/08 | **6** | Redação técnica da proposta de pesquisa |
| 8 | &nbsp;&nbsp;&nbsp;&nbsp;2.3 Marco: Entrega formal do Plano de Pesquisa | 0 dias | 04/09 | **7** | Milestone de entrega exigida pela coordenação |
| **9** | &nbsp;&nbsp;**3. Capacitação Técnica e Alinhamento** | 35 dias | 05/09 | - | *Fase de estudos do Spec-Kit e monografia* |
| 10 | &nbsp;&nbsp;&nbsp;&nbsp;3.1 Estudo prático de TDD e especificações executáveis (Spec-Kit) | 25 dias | 05/09 | **8** | Aquisição de conhecimento prático e PoCs de teste |
| 11 | &nbsp;&nbsp;&nbsp;&nbsp;3.2 Recebimento do Modelo oficial da Monografia | 0 dias | 07/10 | - | Milestone de recebimento do padrão institucional |
| 12 | &nbsp;&nbsp;&nbsp;&nbsp;3.3 Reuniões semanais com a Orientadora | 110 dias | 02/07 | - | Encontros regulares de orientação (todas as quintas) |
| **13** | &nbsp;&nbsp;**4. Integração Externa e Decisão do Mock** | 20 dias | 24/09 | - | *Fase de definição de integração com a certificadora* |
| 14 | &nbsp;&nbsp;&nbsp;&nbsp;4.1 Contato e tentativa de integração de APIs com prestadora | 15 dias | 24/09 | - | Tentativa de alinhamento técnico com a certificadora |
| 15 | &nbsp;&nbsp;&nbsp;&nbsp;4.2 Reunião de decisão técnica: Construção do serviço Mock | 2 dias | 16/10 | **14** | Decisão arquitetural após inviabilidade de APIs |
| 16 | &nbsp;&nbsp;&nbsp;&nbsp;4.3 Desenvolvimento do simulador Mock da certificadora | 7 dias | 20/10 | **15** | Implementação do mock do fornecedor de calibrações |
| 17 | &nbsp;&nbsp;&nbsp;&nbsp;4.4 Marco: Entrega da 1ª versão do simulador Mock | 0 dias | 27/10 | **16** | Milestone de disponibilização do serviço Mock |
| 18 | &nbsp;&nbsp;&nbsp;&nbsp;4.5 Testes de integração do Mock e refinamentos de dados | 8 dias | 28/10 | **17** | Validação do fluxo assíncrono e cenários de erro |
| **19** | &nbsp;&nbsp;**5. Desenvolvimento dos Microsserviços (Java/Spring)** | 35 dias | 18/10 | - | *Fase de codificação dos serviços e regras* |
| 20 | &nbsp;&nbsp;&nbsp;&nbsp;5.1 Modelagem e implementação dos microsserviços (EDA) | 25 dias | 18/10 | **15** | Microsserviços de inventário, farol e mensageria |
| 21 | &nbsp;&nbsp;&nbsp;&nbsp;5.2 Implementação do algoritmo de batimento com TDD / Spec-Kit | 15 dias | 05/11 | **18, 20** | Regras de validação de certificados e divergências |
| 22 | &nbsp;&nbsp;&nbsp;&nbsp;5.3 Conteinerização dos serviços com Docker | 6 dias | 20/11 | **21** | Criação de Dockerfiles e docker-compose da solução |
| **23** | &nbsp;&nbsp;**6. Documentação e Fechamento** | 45 dias | 08/10 | - | *Fase de escrita final e preparação da banca* |
| 24 | &nbsp;&nbsp;&nbsp;&nbsp;6.1 Redação dos capítulos da Monografia no LaTeX | 35 dias | 08/10 | **11** | Redação dos Capítulos 1 a 6 |
| 25 | &nbsp;&nbsp;&nbsp;&nbsp;6.2 Revisão final com a Orientadora Ramyres e ensaios | 6 dias | 27/11 | **22, 24** | Fechamento da documentação e preparação da banca |
| 26 | &nbsp;&nbsp;&nbsp;&nbsp;6.3 Marco Final: Entrega completa do TCC e Fábrica de Software | 0 dias | 04/12 | **25** | Milestone final de entrega do projeto e monografia |
