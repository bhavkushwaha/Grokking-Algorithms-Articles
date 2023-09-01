## Divide & Conquer (Chapter 4)

In this article we will use 2 Examples to explain the concept of Divide & Conquer.

The First Example will be a visual one and the latter one will be a code one.

## EXAMPLE 1
Suppose you are a farmer with a plot of land. You want to divide this farms evenly into square plots. You want the plots to be as big as possible.

![1680 m x 640 m Farmland](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0ofy9vwaq7hbppxfzfk0.jpg)

The following Constraints are present:-

![Constraints](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xciro894i0eoqc6fci6r.png)

Here to solve the farmer's problem, we will use **Divide & Conquer** Strategy!

The Divide & Conquer Strategy consists of two cases:-

1. **Base Case** : The simplest possible case!

2. **Recursive Case** : Divid eor decrease your problem until it becomes the Base Case.

Now solving the Farmer's problem:

- Let's start by marking out the bigest boxes you can use.

![640x400](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/kr63vnxkcuk4yy5qfms9.png)

You can fit two 640x640 boxes in there and some land is still left to be divided!

- Now, apply the same algorithm to the remaining land!

The biggest box we can create is 400 x 400 m with 400 x 240 remaining area.

![400x240](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/l1jrf8q005vjvm1le5si.png)

- Now mark a box to get an even smaller segment. 

![240x160](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/vbh4xkrmdsue19x3vswp.png)

- Going for an even smaller box!

![160x80](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/zienycsqlc0cmu4m6ohl.png)

- Hey Look! we encountered the **Base Case** !


![80x80](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/0mzyrt3scomxtxg46jyf.png)

- So for the original farm, the biggest plot size you can use is 80 x 80 m.


![final](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/udnz7ddjw124xzwb5luc.png)

## EXAMPLE 2

You are given an array of numbers. You have to add all the numbers and return the total.


![array](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/psd9lywckh6ekbat2n6p.png)

It's pretty easy to do it with a loop:

```
def sum(arr):
 total = 0
 for x in arr:
  total += x
 return total
```
But the challenge is to do it using Recursion!

Follow these steps to solve the problem:-

1 ) Figure out the **Base Case**

Think about the simplest case. Here, if we get an array with 0 or 1 element then thats pretty easy to sum up.

![base case](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/gql05npg0f7n3n7b6qpz.png)

2 ) We need to move more closer to an empty array wit hevery **recursive call**.

![recursive case 1](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/x9dqxzgokmuwrhffkv3u.png)

![recursive case 2](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/amaminraijmvajezoa5t.png)

3 ) Now the **Sum** Function Works :-

- It's Principal :

![principal](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/qx4brwr94woaonespvba.png)

- Sum Function in Action and Recursion taking place :

![Final](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/esgeemodkao35wo7x06d.png)

**Tip:** When we are writing a recursive function involving an array, the base case is often an empty array with one element.



