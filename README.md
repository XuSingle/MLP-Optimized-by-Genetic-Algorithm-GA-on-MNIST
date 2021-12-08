# MLP-Optimized-by-Genetic-Algorithm-GA-on-MNIST
Here is a record about Project 2 in COMP 5511 in H.K. PolyU. </br >
Build MLP and use GA as optimizer to recognize picture from MNIST </br >

We use Geatpy library to call a GA and construct a MLP with only one hidden layer with 100 hidden nodes. </br >
</br>
We split the train set into 6 subsets, this means we will train 6 models to recognize digits.
</br >
</br >
We have:</br>
|  Model   | Accuracy on train set | Accuracy on test set |
|  :----:  |  :----:  |  :----:  |
| Model1(0-10000)  | 0.8217 | 0.7924 |
| Model2(10000-20000)  | 0.8421 | 0.8222|
| Model3(20000-30000)  | 0.8013 | 0.774|
| Model4(30000-40000)  | 0.8078 | 0.7985|
| Model5(40000-50000)  | 0.8074 | 0.7879|
| Model6(50000-60000)  | 0.7934 | 0.7527|
</br >
Now we consider the model combination, we know that in the test set, there are 10,000 pictures, we use combination strategy from the bagging algorithm, the votes.
</br >
</br >
We combine all 6 models' output into a matrix which belongs to 10000*6 dimensions matrix, then select the mode in each line of this matrix, if the mode is not unique, we choose the one with the highest accuracy on the train set. </br >
</br >
After combination, the accuracy of final model is 0.8679.
