# Previsão de Score de Crédito

Este projeto foi desenvolvido como um exercício didático para o curso da EBAC, com o objetivo de aplicar técnicas de machine learning para prever a inadimplência de clientes com base em seus dados.

## 🎯 Objetivo

O objetivo principal deste projeto é construir um modelo de classificação capaz de identificar a probabilidade de inadimplência com base no perfil do cliente. Isso pode ajudar instituições financeiras a minimizar riscos e tomar decisões mais assertivas em relação à concessão de crédito.

## 💾 Conjunto de Dados

O conjunto de dados utilizado neste projeto é de um desafio do Kaggle sobre previsão de aprovação de cartão de crédito. Ele contém 15 variáveis, além da variável alvo, que indica se um cliente é um bom ou mau pagador.

| Nome da Variável      | Descrição                                        | Tipo    |
| --------------------- | ------------------------------------------------ | ------- |
| `sexo`                | M = 'Masculino'; F = 'Feminino'                  | M/F     |
| `posse_de_veiculo`    | Y = 'Sim'; N = 'Não'                             | Y/N     |
| `posse_de_imovel`     | Y = 'Sim'; N = 'Não'                             | Y/N     |
| `qtd_filhos`          | Número de filhos                                 | Inteiro |
| `tipo_renda`          | Tipo de renda (ex: assalariado, autônomo)        | Texto   |
| `educacao`            | Nível de escolaridade (ex: secundário, superior) | Texto   |
| `estado_civil`        | Estado civil (ex: solteiro, casado)              | Texto   |
| `tipo_residencia`     | Tipo de residência (ex: casa/apartamento)        | Texto   |
| `idade`               | Idade em anos                                    | Inteiro |
| `tempo_emprego`       | Duração do emprego em anos                       | Inteiro |
| `possui_celular`      | Indica se o cliente possui celular (1=sim)       | Binário |
| `possui_fone_comercial` | Indica se o cliente possui telefone comercial (1=sim) | Binário |
| `possui_fone`         | Indica se o cliente possui telefone (1=sim)      | Binário |
| `possui_email`        | Indica se o cliente possui e-mail (1=sim)        | Binário |
| `qt_pessoas_residencia` | Número de pessoas na residência                | Inteiro |
| `mau`                 | Indicador de mau pagador (True=mau, False=bom)   | Binário |

## 🛠️ Tecnologias Utilizadas

- **Python 3.8.5**
- **Pandas**
- **Seaborn**
- **Matplotlib**
- **Scikit-learn**

## 📈 Modelo

O modelo foi desenvolvido utilizando a técnica de Random Forest, um algoritmo versátil e robusto que captura eficazmente padrões complexos nos dados.

## 📊 Resultados

O modelo alcançou uma acurácia de **97,67%** na previsão de inadimplência de clientes. A matriz de confusão oferece uma visão mais detalhada dos resultados:

|            | Previsto: Bom | Previsto: Mau |
| ---------- | ------------- | ------------- |
| **Real: Bom**  | 16042         | 165           |
| **Real: Mau**   | 243           | 1082          |

Isso indica um alto nível de acurácia na identificação de bons e maus pagadores, embora com uma leve tendência a classificar incorretamente maus pagadores como bons.

## 🚀 Melhorias Futuras

- **Engenharia de Features**: Criar novas variáveis a partir das existentes para melhorar o poder preditivo do modelo.
- **Ajuste de Hiperparâmetros**: Otimizar os parâmetros do Random Forest para alcançar resultados ainda melhores.
- **Modelos Alternativos**: Testar outros algoritmos de classificação, como Gradient Boosting ou Support Vector Machines (SVM), para comparar seus desempenhos.
- **Implantação em Produção**: Implementar o modelo em um motor de crédito para automatizar as decisões de aprovação e rejeição de crédito, com uma etapa intermediária para análise manual.
