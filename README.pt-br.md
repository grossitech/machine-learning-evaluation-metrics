# **Projeto: Cálculo de Métricas de Avaliação de Aprendizado em Machine Learning**

## **📖 Sobre o Projeto**

Este repositório contém o estudo e a implementação prática do **Cálculo de Métricas de Avaliação de Aprendizado**, um tema fundamental na área de Machine Learning. O objetivo deste projeto é demonstrar como avaliar quantitativamente o desempenho de um modelo de classificação.

O estudo teórico e a implementação do código estão consolidados no notebook:  
`Calculation_of_Learning_Evaluation_Metrics_Confusion_Matrix.ipynb`

## **🎯 O Tema: Cálculo de Métricas de Avaliação de Aprendizado**

Após treinar um modelo de Machine Learning, como podemos saber se ele é realmente eficaz? Apenas treinar não é suficiente; precisamos **validar** e **medir** seu desempenho de forma objetiva. É aqui que entram as **métricas de avaliação**.

Métricas são medidas quantificáveis que nos permitem analisar o resultado de um modelo, ou seja, medir sua performance em uma tarefa específica. Para modelos de classificação, a ferramenta central para essa análise é a **Matriz de Confusão**.

### **Matriz de Confusão**

A Matriz de Confusão é uma tabela que visualiza o desempenho de um algoritmo, comparando as classes reais com as classes previstas pelo modelo[cite: 49]. Ela nos permite ver não apenas quantos acertos e erros o modelo cometeu, mas também os *tipos* de acertos e erros.

|                | **Classe Predita: Positiva** | **Classe Predita: Negativa** |
| :------------- | :--------------------------: | :--------------------------: |
| **Classe Real: Positiva** |       VP (Verdadeiro Positivo)       |        FN (Falso Negativo)       |
| **Classe Real: Negativa** |       FP (Falso Positivo)        |       VN (Verdadeiro Negativo)       |

* **VP (Verdadeiro Positivo):** Acerto. O modelo previu "Positivo" e o real era "Positivo".
* **VN (Verdadeiro Negativo):** Acerto. O modelo previu "Negativo" e o real era "Negativo".
* **FP (Falso Positivo):** Erro do Tipo I. O modelo previu "Positivo", mas o real era "Negativo".
* **FN (Falso Negativo):** Erro do Tipo II. O modelo previu "Negativo", mas o real era "Positivo".

A partir desses quatro valores, podemos calcular diversas métricas para entender o comportamento do nosso modelo.

A partir desses quatro valores, podemos calcular diversas métricas para entender o comportamento do nosso modelo.

### **Principais Métricas de Avaliação**

As seguintes métricas foram estudadas e implementadas no projeto:

#### **1\. Acurácia (Accuracy)**

Mede o percentual geral de acertos do modelo. É a métrica mais simples, mas pode ser enganosa em datasets desbalanceados.

* **Fórmula:** `(VP \+ VN) / (VP \+ VN \+ FP \+ FN)`

#### **2\. Precisão (Precision)**

Dentre todas as vezes que o modelo previu a classe "Positiva", quantas ele realmente acertou? É uma métrica importante quando o custo de um Falso Positivo é alto.

* **Fórmula:** `VP / (VP \+ FP)`

#### **3\. Sensibilidade (Recall ou Revocação)**

Dentre todos os casos que eram realmente "Positivos", quantos o modelo conseguiu identificar? É crucial quando o custo de um Falso Negativo é alto.

* **Fórmula:** `VP / (VP \+ FN)`

#### **4\. Especificidade**

Dentre todos os casos que eram realmente "Negativos", quantos o modelo conseguiu identificar?

* **Fórmula:** `VN / (VN \+ FP)`

#### **5\. F1-Score**

É a média harmônica entre a Precisão e a Sensibilidade. É uma ótima métrica para ter uma visão balanceada do desempenho, especialmente quando as classes são desiguais.

* **Fórmula:** `2 * [(Precisão * Sensibilidade) / (Precisão + Sensibilidade)]`

## **💻 Implementação Prática**

O estudo e a aplicação prática de todos esses conceitos estão detalhados no notebook Jupyter `Calculation_of_Learning_Evaluation_Metrics_Confusion_Matrix.ipynb`.

No notebook, você encontrará:

* A simulação de dados de um modelo de classificação.  
* A geração da Matriz de Confusão usando a biblioteca Scikit-learn.  
* A extração dos valores de VP, VN, FP e FN da matriz gerada.  
* O cálculo e a exibição de todas as métricas de avaliação discutidas acima.

## **⚙️ Como Executar o Projeto**

1. Clone este repositório.  
2. Abra o arquivo .ipynb no Google Colab, Jupyter Notebook ou qualquer ambiente compatível.  
3. Execute as células em ordem para ver a geração da matriz de confusão e o cálculo das métricas.

## 👨‍💻 Author

<img 
  align=left 
  margin=10 
  width=80 
  src="https://avatars.githubusercontent.com/u/188269406"
/>
<p>&nbsp&nbsp&nbsp&nbspLuciano Grossi<br/><br/>
    &nbsp&nbsp&nbsp
    <a href="https://github.com/grossitech"><img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
    <a href="https://twitter.com/lucianogrossi"><img src="https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white" alt="Twitter"></a>
    <a href="https://www.linkedin.com/in/lucianogrossi"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
</p>

---

## 📜 License

This project is under the MIT License. See the [LICENSE](LICENSE) file for more details.