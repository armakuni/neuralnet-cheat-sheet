# Flow Charts to make Machine Learning Easier

**Note:** these are rules of thumb 👍, not hard laws. They are designed for people (well me, it's mostly designed for [me](https://github.com/PurpleBooth)) from a software development world who are learning about 🖥️ machine learning 🧑‍🏫, to stop them from getting unexpected results. 

More experienced 🔢mathemagicians✨ or 👨‍🔬 data scientists 👩‍🔬 might recommend something else.

## Problem Selection

First question is do you need a neural net. They aren't always the best thing


```mermaid
graph TD
    START[What algorythm should I use?] --> LABEL{"Does your data already have an<br />answer (or label) column?"}
    LABEL -->|No| CLUSTERING[Use clustering]
    LABEL -->|Yes| IMPROVE{"Do you already have a model<br />you want to improve?"}
    IMPROVE -->|"Yes"| CARE{"What do you care about?"}
    CARE -->|Speed| SPEED[Random Search]
    CARE -->|Accuracy| ACC[Grid Search]
    IMPROVE -->|"No"| LINEAR{"Plot your data<br />onto a graph<br />can you seperate it<br />with a straight line?"}
    LINEAR -->|"No"| NN["Use a neural net"]
    LINEAR -->|"Yes"| LR["Linear Regression"]
```


## Neural Nets

It looks like a neural net is your best option, how should it be setup?

### What activation function should I use?

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

### What metric function should I use?

```mermaid
graph TD
    A[What metric function should I use?] --> B{"What's the question?"}
    B -->|"Is this a or b or c or d or ... ?<br />Classification"| C[Use Accuracy]
    B -->|Something else| D[Use Loss]
```


### What loss function should I use?

```mermaid
graph TD
    A[What loss function should I use?] --> B{"What's the question?"}
    B -->|"Is this a or b<br />Binary classification"| C[Binary Crossentropy]
    B -->|"Is this a or b or c or d or ... ?<br />Multi-classification"| D[Categorical Crossentropy]
    B -->|"Something else"| E[Mean Absolute Error]
```
