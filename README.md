# **Project: Calculation of Machine Learning Evaluation Metrics**

> 📌 This is the English version of the README.  
> Você também pode ler a versão em português aqui: [README.pt-br.md](README.pt-br.md)

## **📖 About the Project**

This repository contains the study and practical implementation of the **Calculation of Learning Evaluation Metrics**, a fundamental topic in the field of Machine Learning.  
The goal of this project is to demonstrate how to quantitatively evaluate the performance of a classification model.

The theoretical study and code implementation are consolidated in the notebook:  
`Calculation_of_Learning_Evaluation_Metrics_Confusion_Matrix.ipynb`

## **🎯 The Topic: Calculation of Learning Evaluation Metrics**

After training a Machine Learning model, how can we know if it is truly effective? Training alone is not enough; we must **validate** and **measure** its performance objectively.  
This is where **evaluation metrics** come in.

Metrics are quantifiable measures that allow us to analyze the outcome of a model, i.e., to measure its performance on a specific task. For classification models, the central tool for this analysis is the **Confusion Matrix**.

### **Confusion Matrix**

The Confusion Matrix is a table that visualizes the performance of an algorithm by comparing the actual classes with the classes predicted by the model.  
It allows us to see not only how many correct and incorrect predictions the model made, but also the *types* of correct and incorrect predictions.

|                | **Predicted: Positive** | **Predicted: Negative** |
| :------------- | :---------------------: | :---------------------: |
| **Actual: Positive** |       TP (True Positive)       |        FN (False Negative)       |
| **Actual: Negative** |       FP (False Positive)      |       TN (True Negative)        |

* **TP (True Positive):** Correct. The model predicted "Positive" and the actual was "Positive".  
* **TN (True Negative):** Correct. The model predicted "Negative" and the actual was "Negative".  
* **FP (False Positive):** Type I Error. The model predicted "Positive" but the actual was "Negative".  
* **FN (False Negative):** Type II Error. The model predicted "Negative" but the actual was "Positive".  

From these four values, we can calculate several metrics to better understand the behavior of our model.

### **Main Evaluation Metrics**

The following metrics were studied and implemented in this project:

#### **1. Accuracy**

Measures the overall percentage of correct predictions. It is the simplest metric but can be misleading in imbalanced datasets.  

* **Formula:** `(TP + TN) / (TP + TN + FP + FN)`

#### **2. Precision**

Of all the times the model predicted the "Positive" class, how many were actually correct?  
It is important when the cost of a False Positive is high.  

* **Formula:** `TP / (TP + FP)`

#### **3. Recall (Sensitivity)**

Of all the cases that were actually "Positive," how many did the model correctly identify?  
It is crucial when the cost of a False Negative is high.  

* **Formula:** `TP / (TP + FN)`

#### **4. Specificity**

Of all the cases that were actually "Negative," how many did the model correctly identify?  

* **Formula:** `TN / (TN + FP)`

#### **5. F1-Score**

The harmonic mean between Precision and Recall.  
It is a great metric for a balanced view of performance, especially when classes are unequal.  

* **Formula:** `2 * [(Precision * Recall) / (Precision + Recall)]`

## **💻 Practical Implementation**

The study and practical application of all these concepts are detailed in the Jupyter Notebook:  
`Calculation_of_Learning_Evaluation_Metrics_Confusion_Matrix.ipynb`

In the notebook, you will find:

* A simulation of classification model data.  
* Generation of the Confusion Matrix using the Scikit-learn library.  
* Extraction of TP, TN, FP, and FN values from the generated matrix.  
* Calculation and display of all evaluation metrics discussed above.  

## **⚙️ How to Run the Project**

1. Clone this repository.  
2. Open the `.ipynb` file in Google Colab, Jupyter Notebook, or any compatible environment.  
3. Run the cells in order to see the generation of the confusion matrix and the calculation of the metrics.  

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
