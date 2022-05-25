# Machine Learning

## Learning
- Learning denotes changes in a system to do the same task more efficiently next time. - (Herbert Simon)
- Making useful changes in our minds. - (Marvin Minsky)


### Traditional Programming vs Machine Learning
- Traditional programming: `data + program => Output`
- Machine Learning: `data + output => Trained Model`

## Machine Learning Definition
- Field of study that gives computer the ability to learn without being explicitly programmed.
- A computer program is said to learn form experience `E` w.r.t to task `T`, and some performance measure `P`, improves with experience `E`.
- `Wiki:` Machine Learning is subfield of Artificial Intelligence that is concerned with the design and development of the algorithms that improve over their performance over time based on data.
- Relates with: Data mining, statistics, inductive reasoning, and theoretical computer science.
---
## When to use ML?
- `When patterns exist in our data:`
  - Even if we don't know what they are.
- `We can not pin down the functional relationships mathematically:`
  - Or we would just code up the algorithm.
- `When we have lots of 'unlabeled' data:`
  - Data is of high dimensions.
  - Labeled data sets are harder to come by.

## Learning in AI
- Essential for unknown environments.
- Learning is useful.
- Learning can modify the agent's decision making mechanisms to improve performance.
- Understand and improve the efficiency of human learning.
- Discover new things or structure that is unknown to human.
- Fill in skeletal or incomplete information about a domain.
- Build software agents that can adapt to their users or to other agents.

## Learning Element
### Design of a learning element is affected by:
- Which components of the performance element are to be learned.
- What feedback is available to learn these components.
- What representation is used for the components.
### Types of feedback:
- `Supervised Learning:` Correct answers for each example.
- `Unsupervised Learning:` Correct answers not given.
- `Reinforcement Learning:` Occasional rewards.

## Three Important Roles of Machine Learning
1) `Data Mining:` Use of historical data to improve decisions.
2) `Software Application:` Speech recognition software.
3) `Self Customizing Programs:` Newsreader app.

## Machine Learning Tasks
- `Categorization:` Learn why certain objects are categorized in that way.
- `Prediction:` Learn how to predict and categorize unseen data.

## Potentials for Machine Learning
- Agents can learn from these examples:
  - Which chemicals are toxic?
  - Which patients have a decease?
  - Which vehicles are tanks?

## Examples of Machine Learning Problems
- `Pattern Recognition`
- `Optimization`
- `Pattern Generation`
- `Anomaly Detection`
- `Prediction`

## Performing Machine Learning
- Specify your problem as a learning task.
- Choose the representation scheme.
- Choose the learning method.
- Apply the learning method.
- Evaluate.

## Supervised Machine Learning
- Input sample (X) and output sample (Y) is given.
- `Y=f(X)`
- We would like to learn f and evaluate it on new data.
### Types
- `Classification:` y is discrete.
- `Regression:` y is continuos. Like linear regression.
- Examples: Is this image of a dog? Cat?, Is this email spam?

### Usefulness of Supervised Machine Learning
- `Classification:` Identifying the class of the data. This predicts a discrete value.
- `Regression:` This provides the continuous data.

### Supervised Learning
- Having lot of labeled data.
- Fully labeled means each example in the dataset contains the answer.
- When new object is given, algorithm should compare it to previous data and predict.
- `Accuracy = number of correct classifications / number of test cases` 

### Dataset
- `Training Set:` Examples used for learning where the target value is known.
- `Validation Set:` Set of examples used to estimate the error. 
- `Test Set:` Used only to access the performances of a classifier.

--- 

## Unsupervised Machine Learning
- Given only samples X of the data, we compute a function f such that `y = f(X)` is “simpler”.
- `Clustering:` y is discrete.
- Y continuous, Matrix Factorization, Kalman filtering, unsupervised neural networks.

### Examples of Unsupervised Learning
- Cluster some hand-written data into 10 classes.
- Top 20 topics on Twitter right now.

### Data Organization in Unsupervised Learning
- `Clustering:`
- `Anomaly Detection:`
- `Association:`