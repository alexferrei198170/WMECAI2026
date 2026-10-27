# WMECAI 2026 - Otimização da Destinação da Produção de Laranja

Repositório referente ao trabalho apresentado no V Workshop de Matemática, Estatística e Computação Aplicadas à Indústria (CEMEAI / ICMC-USP). 

O projeto contém um modelo de Programação Linear desenvolvido para apoiar a tomada de decisão na destinação de safras de laranja entre o mercado interno (fruta *in natura*) e a indústria de suco.

## Descrição do Problema

O modelo aloca uma produção prevista de 100.000 toneladas de laranja considerando as seguintes variáveis operacionais:
* Sazonalidade dos preços.
* Janelas de postergação de colheita (até 10 dias para mercado interno; até 20 dias para indústria).
* Capacidade máxima do mercado interno (12.000 toneladas).
* Compromisso mínimo de entrega para a indústria (40.000 toneladas).
* Balanço de massa e perecibilidade da fruta.

O objetivo da função é a maximização da receita total do produtor.

## Tecnologias Utilizadas

* **Linguagem:** Python
* **Solucionador (Solver):** GurobiPy (Algoritmo Simplex)
* **Manipulação de Dados:** pandas
* **Visualização:** matplotlib

## Metodologia

O problema foi modelado matematicamente com a seguinte função objetivo:

$$Z = \sum_{t \in T} P_{M_t} M_t + \sum_{t \in T} P_{I_t} I_t$$

Foram simulados quatro cenários para análise de sensibilidade:
1. Cenário Base
2. Mercado -15% (queda no preço interno)
3. Indústria +20% (alta no preço industrial)
4. Janela Reduzida (menor margem de postergação da colheita)

## Como Executar

1. Certifique-se de ter o Python instalado.
2. Instale as dependências listadas:
   ```bash
   pip install gurobipy pandas matplotlib
   ```
3. É necessário possuir uma licença válida do Gurobi configurada no ambiente.
4. Execute o script principal do modelo:
   ```bash
   Wmecai2026_Trabalho_Laranja.ipynb
   ```

## Autores

* Alexander Ferreira (ICMC-USP) - ferreira.alexander@aol.com
* Leandro de Andrade (ICMC-USP) - andradeleandro@usp.br

## Agradecimentos e Fontes de Dados

Dados baseados nos relatórios e indicadores do IBGE, Fundecitrus e CEPEA/ESALQ-USP (2025/2026).