# ⚡ ChargeGrid Intelligence: Prova de Conceito (Sprint 2)

Orquestrando a mobilidade elétrica com Dados, IoT e Inteligência Artificial.

---

## 👥 Integrantes

- **RM 571836**	- Bruna Yukimy Hada	
- **RM 571562**	- Denize Ferrante	
- **RM 570436**	- Gabriel Del Pizzo Pintor	
- **RM 572395**	- Gabriel Dias Menezes	
- **RM 570540**	- Ian Rodrigues Martins	
-  **RM 572899** - Patrick Fernandes Martins Pais

---

## 📋 Visão Geral

Este repositório contém a Prova de Conceito (PoC) funcional do **ChargeGrid Intelligence**, uma solução de gestão energética para eletropostos comerciais desenvolvida para o **EV Challenge 2026** em parceria com a **GoodWe** e **FIAP**.

O projeto evolui do planejamento teórico da Sprint 1 para um ambiente de simulação que demonstra a orquestração de potência, faturamento dinâmico e suporte por IA.

Este repositório contém a **Prova de Conceito (PoC) funcional** do **ChargeGrid Intelligence**, uma solução de gestão energética para eletropostos comerciais desenvolvida para o **EV Challenge 2026** em parceria com a **GoodWe** e **FIAP**.

O projeto evolui do planejamento teórico da Sprint 1 para um ambiente de simulação que demonstra:
- ⚡ Orquestração inteligente de potência
- 🌡️ Economia em caso de Projeto de Conforto Térmico
- 🔄 Carregamento EV - KM em kWh
- 🌱 Simulação de Emissão de Carbono: EV vs. Gasolina

**Desenvolvido em Google Colaboratory** para máxima acessibilidade e escalabilidade.

---

## 🚀 Executar no Google Colab

Este projeto foi desenvolvido **100% em Google Colaboratory** e pode ser executado diretamente no navegador, **sem necessidade de instalação local**.

### ⚡ Abrir Agora

[![Abrir no Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/seu-usuario/chargegrid-intelligence/blob/main/notebooks/Sprint_2_ChargeGrid.ipynb)

### 📖 Instruções de Execução

1. **Clique no botão acima** para abrir o notebook no Google Colab
2. **Autentique-se** com sua conta Google (se necessário)
3. **Selecione o tipo de ambiente** (opcional):
   - Vá em **Ambiente de Execução > Alterar tipo de ambiente de execução**
   - Selecione **GPU** para melhor performance (recomendado)
4. **Execute as células** sequencialmente:
   - Use **Shift + Enter** para executar cada célula
   - Ou clique em **Ambiente de Execução > Executar tudo**

---

## 🚀 O Problema Central

Eletropostos comerciais enfrentam a ausência de mecanismos integrados para:

- ⚡ Gerenciar potência de forma inteligente
- 📊 Registrar ciclos de carregamento de forma estruturada
- 💳 Aplicar faturamento interoperável

A solução proposta atua como um **hub de inteligência** que transforma carregadores residenciais (Linha HCA G2) em ativos rentáveis e sustentáveis para o varejo.

---

## 🏗️ Arquitetura da Solução

O sistema opera em uma arquitetura híbrida de **três níveis**:

| Camada | Descrição | Tecnologia |
| :--- | :--- | :--- |
| **Física** | Hardware GoodWe HCA G2 e Smart Meters monitorando consumo | Modbus Protocol |
| **Conectividade** | Middleware (Gateway em Python) com consultas periódicas ao portal SEMS Plus | Modelo Pull |
| **Digital** | Lógica de orquestração, tarifação dinâmica e Síndico Virtual (IA) | RAG + GPT-4o-mini |

---

## 💡 Pilares Implementados na PoC

### 1. ⚡ Simulação de Orquestração de Energia /Gerenciamento Inteligente de Demanda (DLM)

simula um sistema de gestão de energia (EMS) para uma galeria comercial equipada com painéis solares, sistemas de armazenamento (BESS) e carregadores de veículos elétricos (EVs). O objetivo é otimizar o fluxo energético, maximizando o autoconsumo solar e minimizando custos operacionais.

#### Fases Operacionais

| Fase | Período | Característica Principal |
| :--- | :--- | :--- |
| Pré-op | Manhã | Carregamento de baterias e preparação da demanda |
| Operacional | Dia | Geração solar ativa, carga de EVs e suporte à rede |
| Noturno | Noite | Descarga de baterias para suprir carga base |

#### Hierarquia de Prioridades de Despacho

| Prioridade | Destino da Energia | Objetivo |
| :--- | :--- | :--- |
| 1 | Carga Crítica | Garantir continuidade da galeria |
| 2 | Carregadores EV | Atender demanda de mobilidade |
| 3 | Baterias (BESS) | Armazenar excedente solar |
| 4 | Rede Elétrica | Exportar excedente (venda) |

#### Resultados da Simulação
O código processa séries temporais de irradiação solar e demanda de carga, retornando:
1. **Perfil de Carga:** Gráficos de consumo vs. geração.
2. **Estado de Carga (SoC):** Evolução do nível das baterias.
3. **KPIs Financeiros:** Economia gerada e eficiência do sistema.

---

### 3.🌡️ Economia em caso de Projeto de Conforto Térmico

## Simulação de Eficiência Energética e Conforto Térmico

Este código realiza uma análise financeira e técnica para otimizar o consumo energético em galerias comerciais. O objetivo é equilibrar o conforto térmico dos ocupantes com a viabilidade econômica de tecnologias sustentáveis.

## Potencial de Redução de Carga Térmica

| Medida | Redução Estimada |
| :--- | :--- |
| Isolamento Térmico | 15% |
| Vidros de Controle Solar | 20% |
| Sombreamento Externo | 25% |
| Ar-Condicionado Eficiente | 30% |
| Automação Inteligente | 10% |

## Resultados da Simulação

O script processa os dados de entrada e retorna:
- **Economia Anual:** Valor monetário economizado em custos operacionais.
- **Economia em 10 Anos:** Projeção do retorno sobre o investimento (ROI).
- **Vagas Adicionais:** Capacidade de carregamento de veículos elétricos viabilizada pelo excedente energético.

---

### 4. 🔄 Carregamento EV - KM em kWh

## Simulação de Custos de Carregamento de Veículos Elétricos (EV)

Este script realiza a conversão precisa de quilometragem percorrida para consumo de energia (kWh) e estima os custos operacionais, permitindo uma análise comparativa direta entre veículos elétricos e a combustão.

### Modelos Suportados

| Modelo | Consumo Médio (kWh/km) |
| :--- | :--- |
| Tesla Model 3 | 0.15 |
| Tesla Model Y | 0.17 |
| Nissan Leaf | 0.16 |
| Chevrolet Bolt | 0.16 |
| BMW i3 | 0.14 |

### Parâmetros e Fórmulas

| Parâmetro | Fórmula / Descrição |
| :--- | :--- |
| Consumo (kWh) | Distância (km) × Consumo Médio (kWh/km) |
| Custo Carregamento | Consumo (kWh) × Tarifa de Energia (R$/kWh) |
| Economia vs Gasolina | (Custo Gasolina) - (Custo EV) |
| % de Economia | (Economia / Custo Gasolina) × 100 |

### Resultados Calculados
O código processa os dados de entrada e retorna:
1. **Consumo Total:** Energia necessária em kWh.
2. **Custo de Carregamento:** Valor financeiro gasto na recarga.
3. **Comparativo:** Economia absoluta em relação a um veículo a combustão.
4. **Eficiência:** Percentual de redução de custos operacionais.

---

### 5.🌱 Simulação de Emissão de Carbono: EV vs. Gasolina

Este código realiza uma análise comparativa entre veículos elétricos (EV) e veículos a combustão (gasolina), calculando o impacto ambiental com base na quilometragem percorrida e nos fatores de emissão específicos do Brasil.

### 1. Fatores de Emissão Utilizados

| Parâmetro | Valor/Unidade |
| :--- | :--- |
| Fator Emissão Brasil (Grid) | 0.06 kg CO2/kWh |
| Fator Emissão Gasolina | 0.12 kg CO2/km |
| Absorção por Árvore | 22 kg CO2/ano |
| Equivalência Voo | 0.25 kg CO2/km |

### 2. Parâmetros e Fórmulas de Cálculo

| Cálculo | Fórmula |
| :--- | :--- |
| Emissão EV | (km / consumo_km_kwh) * fator_grid |
| Emissão Gasolina | km * fator_gasolina |
| Redução | Emissão Gasolina - Emissão EV |
| % Redução | (Redução / Emissão Gasolina) * 100 |

### O que o código calcula:
O script processa os dados de entrada e retorna:
* **🌍 Emissão Total (kg CO2):** Comparativo direto entre os dois modais.
* **📉  Redução de Emissão:** O ganho ambiental líquido ao optar pelo EV.
* **🌱 Equivalência em Árvores:** Quantidade de árvores necessárias para compensar a emissão evitada.
* **✈️ Equivalência em Voo:** Distância aérea equivalente ao impacto evitado.

---















