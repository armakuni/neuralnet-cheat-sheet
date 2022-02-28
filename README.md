# Flow Charts to make Machine Learning Easier

```mermaid
graph TD
    A[What activation function should I use?] --> B{"What kind of node is it?"}
    B -->|Hidden| C[Use Relu]
    B -->|Output| D{"What's the question?"}
    D -->|"Is this a or b<br />Binary classification"| E[Sigmoid]
    D -->|"Is this a or b or c or d or ... ?<br />Multi-classification"| F[Softmax]
    D -->|"Predict a number greater than 0<br />Regression"| C[Use Relu]
    D -->|"Predict a number less than 0<br />Regression"| G[Use Linear]
```
