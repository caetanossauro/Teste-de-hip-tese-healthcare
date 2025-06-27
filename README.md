# Análise de Dados de Saúde: Impacto da Idade no Tempo de Internação Hospitalar

## Visão Geral do Projeto

Este projeto de análise de dados explora o impacto da idade no tempo de internação de pacientes em um hospital específico ("Phillips LLC"). Utilizando um conjunto de dados de saúde, o objetivo é aplicar técnicas de pré-processamento de dados e realizar um teste de hipóteses para determinar se há uma diferença significativa no tempo de internação entre pacientes mais jovens e mais velhos.

## Objetivo Principal

* Investigar a relação entre a faixa etária e a duração da internação hospitalar.
* Aplicar um teste de hipóteses não paramétrico (Mann-Whitney U) para validar estatisticamente a relação observada.

##Insights chave

* Este projeto nos permitiu investigar se a idade do paciente está relacionada ao tempo de internação hospitalar no 'Phillips LLC'. Nossas análises, baseadas no teste de Mann-Whitney U, revelaram o seguinte:

* Identifiquei **evidências estatisticamente significativas** de que pacientes com 60 anos ou mais tendem a ter um tempo de internação *maior* em comparação com pacientes abaixo de 60 anos."

* Estes achados são mais do que apenas números; eles possuem **implicações importantes para a gestão de recursos em saúde, o planejamento de leitos e a otimização do atendimento ao paciente**, especialmente em populações que estão envelhecendo.

## Como Executar o Projeto
Acesse: https://www.kaggle.com/code/caetanossauro/teste-de-hipostes-healthcare


## Metodologia e Análise

1.  **Carregamento e Pré-processamento dos Dados:**
    * Leitura do dataset `healthcare_dataset.csv`.
    * Filtragem de dados para o hospital "Phillips LLC".
    * Tratamento de valores ausentes (`dropna()`).
    * Cálculo do tempo de internação em dias a partir das datas de admissão e alta.
      
2.  **Criação dos Grupos de Análise:**
    * Pacientes divididos em dois grupos com base na idade:
        * **Grupo A:** Pacientes com idade abaixo de 60 anos (`Age < 60`).
        * **Grupo B:** Pacientes com idade igual ou superior a 60 anos (`Age >= 60`).
          
3.  **Definição das Hipóteses:**
    * **Hipótese Nula (H₀):** A mediana do tempo de internação para pacientes com idade inferior a 60 anos é igual à mediana para pacientes com 60 anos ou mais.
    * **Hipótese Alternativa (H₁):** A mediana do tempo de internação para pacientes com 60 anos ou mais é *maior* do que para pacientes com idade inferior a 60 anos.
      
4.  **Teste de Hipóteses:**
    * Foi utilizado o **Teste de Mann-Whitney U** (não paramétrico) para comparar as medianas dos tempos de internação entre os dois grupos.
    * Nível de significância ($\alpha$) adotado: 0.05.
  
## Resultados e Conclusão 

* **Estatística U:** 14.0
* **P-valor:** 0.60

Com base no p-valor 0.60 e no nível de significância de 0.05:
[  **Se p-valor < 0.05:** ]
    Rejeitamos a hipótese nula. Há evidências estatísticas de que o tempo de internação para pacientes com 60 anos ou mais é significativamente maior do que para pacientes com menos de 60 anos neste hospital.
[  **Se p-valor >= 0.05:** ]
    Não rejeitamos a hipótese nula. Não há evidências estatísticas suficientes para afirmar que o tempo de internação é maior para pacientes com 60 anos ou mais neste hospital.

## Tecnologias Utilizadas

* Python
* Pandas (manipulação de dados)
* NumPy (operações numéricas)
* SciPy (teste de hipóteses estatístico)

## Autor

* **Cleidson Santos Oliveira** - [LinkedIn](https://www.linkedin.com/in/cleidson-oliveira-7b7248215/) - [GitHub](https://github.com/caetanossauro).

## Licença

Este projeto está licenciado sob a Licença Apache 2.0 license - veja o arquivo (https://www.apache.org/licenses/LICENSE-2.0.txt) para detalhes.
