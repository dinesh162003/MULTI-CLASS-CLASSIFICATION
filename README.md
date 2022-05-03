### EX NO: 03
### DATE: 08-04-2022
# <p align="center">MULTI-CLASS-CLASSIFICATION</p>
## AIM:
To write a python program to implement the multi class classification algorithm .

## EQUIPMENTS REQUIRED:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner / Google Colab

## RELATED THEORITICAL CONCEPTS:

Neural networks reflect the behaviour of the human brain. They allow programs to recognise patterns and solve common problems in machine learning. This is another option to either perform classification instead of logistics regression.

Classification is categorizing objects into groups. There are different types of classifications one of which is multiclass classification.In multi-class classification, the neural network has the same number of output nodes as the number of classes. Each output node belongs to some class and outputs a score for that class.

Class is a category for example Predicting animal class from an animal image is an example of multi-class classification, where each animal can belong to only one category.

Scores from the last layer are passed through a SoftMax layer. The SoftMax layer converts the score into probability values. At last, data is classified into a corresponding class, that has the highest probability value (max P1).
![nn3](https://user-images.githubusercontent.com/75235159/164048132-f69a4d9c-428d-4b86-8cb0-c62e66a90735.png)


## ALGORITHM
1.Import necessary libraries from packages.

2.Assign x,y values from the given dataset by sklearn.

3.Count the number of key-value pairs in the datasets using counter libraries.

4.Plot the x and y values in the chart using mathplotlib.pyplot

5.Label the values of x and y axis and add title to the graph .

6.Save the file and execute the program.

## PROGRAM:
```
/*
Program to implement the multi class classifier.
Developed by: S. DINESH
RegisterNumber:  212220230011
*/
from numpy import where
from collections import Counter
from sklearn.datasets import make_blobs
from matplotlib import pyplot
X,y=make_blobs(n_samples=1000,centers=3,random_state=1)
print(X.shape,y.shape)
counter=Counter(y)
print(counter)
for i in range(10):
    print(X[i],y[i])
for label,_ in counter.items():
    row_ix=where(y==label)[0]
    pyplot.scatter(X[row_ix,0],X[row_ix,1],label=str(label))
pyplot.legend()
pyplot.show()
```

## OUTPUT:

![NN3B](https://user-images.githubusercontent.com/75235159/164048090-d7135efc-2b32-4b7b-8174-864be821f400.png)

## RESULT:
Thus the python program to implement the multi class classification was implemented successfully.
