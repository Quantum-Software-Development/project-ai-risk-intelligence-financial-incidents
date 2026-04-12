

<br>
 
 \[[🇧🇷 Português](README.pt_BR.md)\] \[**[🇬🇧 English](README.md)**\]
 


<br><br>

# AI Incidents in Financial Services

Análise de Viés Algorítmico, Risco Operacional e Governança de IA em Serviços Financeiros

<br><br>

## Table of Contents

1. [Project Overview](#project-overview)  
   1.1 [Business Context](#business-context)  
   1.2 [General Objective](#general-objective)  
   1.3 [Specific Objectives](#specific-objectives)  
   1.4 [Research Questions](#research-questions)  

2. [Data and Problem Definition](#data-and-problem-definition)  
   2.1 [Data Source: AI Incident Database (AIID)](#data-source-ai-incident-database-aiid)  
   2.2 [Scope: Financial Services Focus](#scope-financial-services-focus)  
   2.3 [Key Raw Variables](#key-raw-variables)  
   2.4 [Core Analytical Concepts](#core-analytical-concepts)  

3. [Derived Variables and Data Model](#derived-variables-and-data-model)  
   3.1 [Financial Application Type (application_type)](#financial-application-type-application_type)  
   3.2 [Incident Type (incident_type)](#incident-type-incident_type)  
   3.3 [Customer Segment (customer_segment)](#customer-segment-customer_segment)  
   3.4 [Severity Level (severity_level)](#severity-level-severity_level)  
   3.5 [Additional Attributes](#additional-attributes)  

4. [Project Structure and Notebooks](#project-structure-and-notebooks)  
   4.1 [Notebook 1 – Data Preparation](#notebook-1--data-preparation)  
   4.2 [Notebook 2 – Exploratory Analysis](#notebook-2--exploratory-analysis)  
   4.3 [Notebook 3 – Feature Engineering and Analytical Base](#notebook-3--feature-engineering-and-analytical-base)  
   4.4 [Notebook 4 – Consolidation and Reporting](#notebook-4--consolidation-and-reporting)  

5. [CRISP-DM Alignment](#crisp-dm-alignment)  

6. [How to Run](#how-to-run)  

7. [Notebook Code (with Graph References)](#notebook-code-with-graph-references)  
   7.1 [Notebook 1 – Data Preparation](#notebook-1--data-preparation-1)  
   7.2 [Notebook 2 – Exploratory Analysis](#notebook-2--exploratory-analysis-1)  
   7.3 [Notebook 3 – Feature Engineering](#notebook-3--feature-engineering-1)  
   7.4 [Notebook 4 – Consolidation and Reporting](#notebook-4--consolidation-and-reporting-1)  

8. [Next Steps and Possible Extensions](#next-steps-and-possible-extensions)  

9. [Author and Context](#author-and-context)  

10. [Topics (Tags)](#topics-tags)


<br><br>

## 1. Visão Geral do Projeto

### 1.1 Contexto de Negócio

Desenvolvemos este projeto sob a perspectiva de uma boutique de consultoria especializada em risco de IA aplicada ao setor financeiro. Nossa proposta é apoiar bancos, fintechs e demais organizações na identificação de padrões de incidente, no mapeamento de vulnerabilidades sistêmicas e na transformação de eventos históricos em inteligência acionável para governança, compliance e mitigação de risco.

O projeto utiliza dados do Artificial Intelligence Incident Database (AIID) para construir uma base analítica focada em serviços financeiros, com ênfase em aplicações como concessão de crédito, detecção de fraude, avaliação de risco, automação bancária, pagamentos, seguros e contextos correlatos. A partir dessa base, estruturamos variáveis analíticas, realizamos exploração descritiva inicial e preparamos o pipeline para análises estatísticas, modelagem preditiva e exposição dos resultados via API ou serviços de dados.

Do ponto de vista de negócio, o problema que endereçamos é a ausência de visibilidade estruturada sobre riscos reais de IA em operações financeiras. Muitas instituições já utilizam modelos algorítmicos em decisões sensíveis, mas ainda carecem de mecanismos robustos para entender onde estão seus maiores riscos, quais aplicações demandam supervisão reforçada, quais grupos podem estar mais expostos a viés e como priorizar controles preventivos com base em evidências.

Nesta fase exploratória, o foco está em organizar a base, criar variáveis derivadas, compreender padrões iniciais e consolidar um pipeline claro, pronto para ser expandido em direção a modelos preditivos, dashboards e APIs.

<br>
