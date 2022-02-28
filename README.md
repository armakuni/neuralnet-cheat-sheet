# Flow Charts to make Machine Learning Easier

## What activation function should I use?

```mermaid
graph TD
    A[What activation function should I use?] --> B{"What kind of node is it?"}
    B -->|Hidden| C[Use Relu]
    B -->|Output| D{"What's the question?"}
    D -->|"Is this a or b<br />Binary classification"| E[Sigmoid]
    D -->|"Is this a or b or c or d or ... ?<br />Multi-classification"| F[Softmax]
    D -->|"Predict a number<br />Regression"| H{What's the output?}
    H -->|"Greater than 0"| C[Use Relu]
    H -->|"Something else"| G[Use Linear]
```


*  https://stackoverflow.com/questions/63883842/can-relu-be-used-at-the-last-layer-of-a-neural-network
*  https://dataaspirant.com/difference-between-softmax-function-and-sigmoid-function/
*  https://patrickhoo.wixsite.com/diveindatascience/single-post/2019/06/13/activation-functions-and-when-to-use-them

## What metric function should I use?

```mermaid
graph TD
    A[What metric function should I use?] --> B{"What's the question?"}
    B -->|"Is this a or b or c or d or ... ?<br />Classification"| C[Use Accuracy]
    B -->|Something else| D[Use Loss]
```


## What loss function should I use?

```mermaid
graph TD
    A[What loss function should I use?] --> B{"What's the question?"}
    B -->|"Is this a or b<br />Binary classification"| C[Binary Crossentropy]
    B -->|"Is this a or b or c or d or ... ?<br />Multi-classification"| D[Categorical Crossentropy]
    B -->|"Something else"| E[Mean Absolute Error]
```
