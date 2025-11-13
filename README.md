# **Global Solution - Dynamic Programming:**

### **Solução: Otimização de Recursos para Requalificação Profissional - Relatório**

# **Nomes e RMs do grupo:**
- Matheus Taylor, RM556211
- Henrique Maldonado, RM557270

# Descrição do Projeto
Este projeto implementa uma solução de otimização para planejamento de requalificação profissional, utilizando algoritmos de ordenação e programação dinâmica para maximizar o valor das habilidades adquiridas dentro de um limite de tempo disponível.

# Contextualização do Problema

## Problema

- Como maximizar o impacto da requalificação profissional considerando restrições de tempo e recursos.

## Entrada

- Lista de 20 habilidades com tempo necessário (horas) e valor de mercado (1-100)
- Capacidade máxima de horas disponíveis para estudo

## Saída

- Valor total máximo alcançável
- Conjunto ótimo de habilidades a serem aprendidas
- Relatório detalhado da solução

## Objetivo

- Maximizar o valor das habilidades adquiridas dentro do limite de tempo disponível.

# Estrutura da Solução

## Tecnologias Utilizadas

- Python como linguagem principal
- Pandas para manipulação de dados
- NumPy para operações numéricas
- Datetime para medição de performance

## Habilidades Disponíveis

O sistema trabalha com 20 habilidades de tecnologia e negócios, incluindo:

- Inteligência Artificial (120h, valor: 95)
- Análise de Dados (80h, valor: 85)
- Programação Python (100h, valor: 90)
- Segurança Cibernética (150h, valor: 92)
- Machine Learning (140h, valor: 96)
- E outras 15 habilidades especializadas

# Funcionalidades Principais

## 1. Algoritmo de Ordenação (Merge Sort Recursivo)

- **Propósito:** Ordenar habilidades por critério específico usando divisão e conquista
- **Recursão:** Divide a lista pela metade até casos base de 1 elemento
- **Complexidade:** O(n log n) garantido

## 2. Problema da Mochila com Recursão e Memoização

- **Propósito:** Resolver problema de otimização com restrições
- **Recursão:** Para cada habilidade, decide incluir ou não na solução
- **Memoização:** Armazena resultados de subproblemas para evitar recálculo
- **Complexidade:** O(n × capacidade)

## 3. Função de Otimização Principal

- **Propósito:** Coordenar todo o processo de otimização
- **Integração:** Combina ordenação com algoritmo da mochila
- **Saída:** Retorna estrutura completa com solução ótima

## 4. Sistema de Relatórios Detalhados

- **Propósito:** Apresentar resultados de forma clara e organizada
- **Análise:** Mostra métricas de eficiência e utilização de recursos

# Como Executar

1. **Pré-requisitos (Instalação da bibleoteca Pandas Numpy)**
   ```bash
   pip install pandas numpy

3. **Execução do Código**
   ```python
   if __name__ == "__main__":
    CAPACIDADE_MAXIMA = 500
    
    print("INICIANDO OTIMIZAÇÃO DE REQUALIFICAÇÃO PROFISSIONAL")
    print(f"Total de habilidades disponíveis: {len(df_habilidades)}")
    print(f"Capacidade máxima: {CAPACIDADE_MAXIMA} horas\n")
    
    df_ordenado = merge_sort_recursivo(df_habilidades, 'tempo')
    print("Habilidades ordenadas por tempo necessário:")
    print(df_ordenado[['nome', 'tempo', 'valor']].to_string(index=False))
    
    inicio = datetime.now()
    resultado = otimizar_requalificacao(df_habilidades, CAPACIDADE_MAXIMA)
    tempo_execucao = (datetime.now() - inicio).total_seconds()
    
    gerar_relatorio_detalhado(resultado, df_habilidades, CAPACIDADE_MAXIMA)
    analisar_eficiencia(df_habilidades)
    
    print(f"\nTempo de execução: {tempo_execucao:.4f} segundos")
   
# Resultados e Relatórios

## Relatório de Otimização

O sistema gera relatórios completos incluindo:

- Capacidade máxima disponível e utilizada
- Valor total alcançado (máximo 200 pontos)
- Lista de habilidades selecionadas
- Eficiência por habilidade (valor/hora)
- Ranking de eficiência geral

## Métricas de Performance

- Tempo de execução: Medido em segundos
- Eficiência algorítmica: O(n log n) para ordenação + O(n × capacidade) para otimização
- Utilização de recursos: Percentual da capacidade total utilizada

# Análise de Eficiência

## Complexidade Computacional

**1. Merge Sort:** O(n log n) - eficiente para ordenação de grandes conjuntos

**2. Problema da Mochila:** O(n × capacidade) - otimizado com memoização

**3. Solução Geral:** Combina as duas abordagens para balance entre performance e precisão

## Vantagens da Abordagem
- Solução Ótima Garantida para o problema da mochila
- Escalabilidade através de algoritmos eficientes
- Flexibilidade para diferentes capacidades e conjuntos de habilidades
- Transparência com relatórios detalhados

# Aplicações Práticas

Este sistema pode ser utilizado por:

- Profissionais buscando planejar sua requalificação
- Empresas desenvolvendo programas de treinamento
- Instituições de ensino otimizando currículos
- Governos planejando políticas de requalificação em larga escala

# Considerações Finais

 A solução implementada demonstra a eficácia de algoritmos clássicos de computação aplicados a problemas reais de otimização de recursos. A combinação de ordenação eficiente com programação dinâmica permite encontrar soluções ótimas mesmo para grandes conjuntos de dados.
 O projeto destaca a importância do pensamento algorítmico na resolução de problemas complexos de alocação de recursos no contexto da transformação digital e requalificação profissional.

