# Flow Charts to make Machine Learning Easier

## What activation function should I use?

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

*  https://stackoverflow.com/questions/63883842/can-relu-be-used-at-the-last-layer-of-a-neural-network
*  https://dataaspirant.com/difference-between-softmax-function-and-sigmoid-function/
*  https://patrickhoo.wixsite.com/diveindatascience/single-post/2019/06/13/activation-functions-and-when-to-use-them

## What metric function should I use?

```mermaid
graph TD
    A[What metric function should I use?] --> B{"What's the question?"}
    B -->|Classification| C[Use Accuracy]
    B -->|Something else| C[Use Loss]
```


## What loss function should I use?

```mermaid
graph TD
    A[What loss function should I use?] --> B{"What's the question?"}
    B -->|"Is this a or b<br />Binary classification"| C[binary crossentropy]
    B -->|"Is this a or b or c or d or ... ?<br />Multi-classification"| D[categorical crossentropy]
    B -->|"Predict a number greater than 0<br />Regression"| E[Mean Absolute Error]
```