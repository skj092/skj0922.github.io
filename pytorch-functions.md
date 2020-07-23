# Pytorch: Your Fevourite Deep Learning Library
**Some most common operation using Pytorch**

Pytorch is an open source machine learning library probably easiest to start with. It is built by Facebook. In this article I will discuess five most common and important funcitons in pytorch.

* Function 1: Transpose
* Funciton 2: Stack
* Function 3: Where
* Function 4: Backward
* Function 5: Add

## Function 1: Transpose
In libear algebra, the transpose of a matrix is an operator which flips a matrix over its diagonal, that is it switches the row and column indices of the matrix by producing. Here we will transpose tensor.

![t1](/images/t1.jpg)

X is a 2-D tensor, we swapped dimension 0 to dimension 1 using torch.transpose()


![t2](/images/t2.png)

We swapped dimension 11 to dimension 0.


![t3](/images/t3.png)

We need to put the dimension which is going to be swapped without. If we put same dimension twice it has no effect.

Transpose function is very useful while matrix multiplication.


## Function 2: Stack
This funciton conconate every new tensor in new dimension. It add every enw tensor to additional dimension.

![s1](/images/s1.png)

Here we stacked b over a and created an additional dimension.

![s2](/images/s2.png)

Here be is the stack of 2 and tensor a.

![s3](/images/s3.png)

To make an stack all tensors need to be in equal size.

While working with image data stack function is useful to numerical calculation. To calculate statistical values like mean, median, etc. Stakcing makes easy to calculate all of these.

## Function 3: Where
Returns tensor of element with given condition.

![w1](/images/w1.png)

torch.where() returns a tensor with values y if x>0 else it return x.

![w2](/images/w2.png)

Here we find the differnece between x and y. This funciton can be used as a loss function is binary classification problems, where the target variable is similar like x and predicted values like y.

![w3](/images/w3.png)

If if size of y is less then x then pytorch automatically expand y to the size of x without additional memory. However if the size of y is greater then x, the it doesn't work.

This function can be used as a loss function in binary classification problems.

## Funciton 5: Add
To add two tensor

![a1](/images/a1.png)

Here add function just work like + operator.

![a2](/images/a2.png)

As you can see above the size of y is not the size of x, but pytorch expands the size of y by replacing its data and do elementwise operation.

![a3](/images/a3.png)

Here the size of y is greator then the size of x but x doesn't expands. Pytorch expands in every dimension, if if increase the dimension of x then it will become 3*3 still doesn't match the size of y. 

It is very halpful while doing tensor operaiton. Additional operator is the  most used operator. 

## Conclusion
We have covered five most useful pytorch funciton. Go through the [pytorch documentation](https://pytorch.org/docs/stable/tensors.html) and write five function of your choice. 

