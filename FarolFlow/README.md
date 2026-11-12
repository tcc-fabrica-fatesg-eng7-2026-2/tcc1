# FarolFlow - Documentação Técnica e Especificações (SDD / Spec-Kit)

Este diretório centraliza a documentação de engenharia de software da plataforma **FarolFlow**, projetada para automatizar e escalonar a gestão do ciclo de calibração metrológica industrial por meio de microsserviços em Java (Spring Boot), conteinerização (Docker) e Arquitetura Orientada a Eventos (EDA).

Esta documentação serve como base executável para o time de desenvolvimento implementar os serviços sob a metodologia **SDD** (*Spec-Driven Development*) e **TDD** (*Test-Driven Development*).

---

## 📁 Estrutura de Documentos

```text
FarolFlow/
├── README.md                     # Visão geral, roteiro e índice da documentação
├── 01_visao_e_dominio.md         # Contexto metrológico, glossário e mapeamento da planilha atual
├── 02_requisitos.md              # Requisitos Funcionais (RF) e Não Funcionais (RNF) com critérios de aceite
├── 03_regras_de_negocio.md       # Algoritmo de batimento, tolerâncias e tratamento de exceções (extravio/baixa)
├── 04_arquitetura_e_eventos.md   # Microsserviços, tópicos/filas, payloads JSON e contratos de mensageria
├── 05_integracao_mock.md         # Especificação da interface com o Mock do prestador de calibração
├── 06_especificacoes_speckit.md  # Cenários BDD/Gherkin (Given/When/Then) prontos para TDD (JUnit)
└── diagramas/                    # Modelos visuais (arquitetura, fluxo de eventos, DER e classes)
```

---

## 🎯 Roteiro de Implementação e Entregas

### Passo 1: Mapeamento de Domínio e Dados Legados (`01_visao_e_dominio.md`)
- Extração dos campos da planilha de controle manual atual (TAG, periodicidade semestral/anual, datas de calibração e vencimento).
- Glossário metrológico (PT-100, manômetros, transmissores de peso, VIM, normas ISO 9001 e ISO/IEC 17025).

### Passo 2: Especificação de Requisitos (`02_requisitos.md`)
- **Requisitos Funcionais (RF):** Ingestão cadastral, geração da projeção do relatório Farol, importação assíncrona de laudos e registro de justificativas de descarte/extravio.
- **Requisitos Não Funcionais (RNF):** Comunicação assíncrona desacoplada via mensageria, conteinerização Docker, idempotência de eventos e tempos de resposta sem degradação transacional.

### Passo 3: Regras de Negócio e Batimento (`03_regras_de_negocio.md`)
- Regras de cálculo de status (No Prazo, Vincendo no Mês/Farol, Vencido).
- Algoritmo de validação cruzada entre dados do certificado (número do certificado, data da calibração, validade) contra a base oficial do FarolFlow.
- Emissão imediata de alertas de divergência cadastral ou desvio metrológico.

### Passo 4: Arquitetura, Microsserviços e Eventos (`04_arquitetura_e_eventos.md`)
- Definição dos microsserviços em Java / Spring Boot.
- Topologia de filas e tópicos de mensageria.
- Schemas JSON dos eventos de domínio:
  - `InstrumentoCadastradoEvent`
  - `CalibracaoAgendadaEvent`
  - `CertificadoRecebidoEvent`
  - `DivergenciaDetectadaEvent`

### Passo 5: Integração com Simulador Externo (`05_integracao_mock.md`)
- Contrato de dados e protocolo de comunicação com o microsserviço Mock da certificadora parceira (Suporty Calibrações).
- Cenários simulados de envio de relatórios provisórios e certificados definitivos (tanto válidos quanto divergentes).

### Passo 6: Especificações Executáveis para Spec-Kit / TDD (`06_especificacoes_speckit.md`)
- Matriz de testes orientada a comportamento (*Behavior-Driven Development* - BDD).
- Cenários *Given / When / Then* prontos para conversão em testes unitários e de integração com JUnit e Spring Test antes do código produtivo.

### Passo 7: Diagramas Técnicos (`diagramas/`)
- Diagrama de Arquitetura de Microsserviços e Mensageria.
- Diagrama de Sequência do fluxo de batimento assíncrono.
- Diagrama de Entidade-Relacionamento (DER) / Modelagem de Dados.
