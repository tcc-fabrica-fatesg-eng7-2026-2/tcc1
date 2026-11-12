# Projeto Integrador: TCC e Fábrica de Software

Este repositório contém o projeto desenvolvido como requisito para as disciplinas de **Trabalho de Conclusão de Curso (TCC)** e **Fábrica de Software**, integrando o curso de **Engenharia de Software** da instituição **SENAI Fatesg**.

## 👥 Equipe Desenvolvedora (Autores)

* Daniel Douglas Melo Gomes Neto
* Jose Carlos Vaz Felipe
* Lucas Alves Dos Reis
* Pedro Henrique Pereira Medeiros Spíndola

---

# Proposta de Trabalho de Conclusão de Curso (TCC)

## Tema
Automatização e Gestão do Ciclo de Calibração de Instrumentos Metrológicos Industriais apoiada em Microserviços (Java / Spring Boot), Conteinerização e Arquitetura Orientada a Eventos de Alta Escalabilidade.

---

## Contextualização e Cenário Atual
Na indústria, a rastreabilidade e a calibração de instrumentos de medição (como manômetros, termorresistências PT-100 e transmissores de peso) são requisitos fundamentais para atendimento às normas de qualidade e auditorias regulatórias (como ISO 9001 e ISO/IEC 17025).

Atualmente, o controle desses instrumentos é realizado por meio de planilhas eletrônicas divididas por periodicidades de calibração (semestral e anual) e geridas sob rigoroso controle de revisões com o time de qualidade. Todo mês é gerada manualmente uma projeção dos instrumentos a vencer (denominada "Farol") para envio à empresa prestadora de serviços de calibração (Suporty Calibrações).

---

## O Problema
O fluxo operacional atual depende de conferências manuais e apresenta gargalos significativos:
1. **Conferência manual de certificados:** A empresa parceira envia relatórios provisórios e posteriormente certificados digitais, exigindo que cada dado (datas de calibração, vencimento e numeração de certificados) seja validado manualmente contra a base interna.
2. **Risco de inconsistências metrológicas:** A validação manual abre margem para erros humanos ou divergências que podem comprometer auditorias de qualidade.
3. **Ausência de visibilidade em tempo real:** Acompanhar o progresso da campanha de calibração (quanto já foi executado vs. o que ainda resta no mês) exige consolidações manuais constantes.
4. **Tratamento de exceções descentralizado:** Instrumentos portáteis extraviados ou descartados demandam justificativas formais que hoje ficam dispersas em e-mails e anotações isoladas.
5. **Gargalo de escalabilidade e sincronização:** À medida que o parque de instrumentos se expande entre diferentes plantas e setores fabris, arquiteturas monolíticas síncronas tornam-se ineficientes para lidar com fluxos contínuos de atualizações de certificados e batimentos volumosos.

---

## Objetivo do Trabalho
Desenvolver uma solução informatizada centralizada para a gestão metrológica, estruturada em **microserviços desenvolvidos em Java com o ecossistema Spring Boot**, devidamente **conteinerizados** e orquestrados sobre uma **Arquitetura Orientada a Eventos (EDA)**, capaz de:
- Servir como a base oficial e confiável de registro dos instrumentos de medição e suas revisões com alta capacidade de expansão e escalabilidade horizontal.
- Processar de forma desacoplada e assíncrona, via mensageria/eventos, o batimento automático entre os dados fornecidos pelo prestador de calibração e a base interna, disparando alertas automáticos sobre incoerências e divergências.
- Monitorar e projetar os vencimentos de calibração com visualização clara do status de execução (planejado vs. executado) por meio de fluxos reativos em tempo real.
- Centralizar o registro e a guarda de evidências para instrumentos não localizados ou baixados.
- Empregar práticas de desenvolvimento guiado por testes e especificações executáveis (**Spec-Kit / TDD**) para blindar as regras de negócio metrológicas.

---
*SENAI Fatesg - Goiânia, 2026*
