
![Cover Image](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/09y8jd7fby1eem3xcpcd.jpg)

## Topics covered in Chapter 3 : Recursion
1. What is Recursion?
2. Base Case & Recursive Case
3. The Stack
4. Call Stack
5. The Call Stack with Recursion

## What is Recursion?
It is Explained using an Example of Grandma's Boxes & Key.

- You want to open your Grandma's suitcase but the key to it is in this Box.

- But this box contains more boxes inside those boxes. And the key is in a box somewhere.

- Here we can use 2 Algorithms to find the key:

1. Using Loops

2. Using Recursion

![An Image have two different approaches for solving the same box-key problem](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/23lhtrakqp11mclkeb5o.png)

Important Points to note:

- There is no 100% guaranteed performance benefit of using recursion, infact sometimes loops perform better.

## Base Case & Recursive Case
Every Recursive Function has two parts:-

Base Case

- Here, the function doesn't call itself and thus this case prevents a chance of infinite loop.

Recursive Case

- Here, the function calls itself again.

![Base Case vs Recursive Case in a Function](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/mh9j5ez1c8rzahn5ei82.png)

## The Stack
The best example to explain a stack is a Todo-List.
It enables two features : 1. Push() & 2. Pop()

![Push & Pop in a stack](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5d7zthz3gofx7f64z430.jpg)

## The Call Stack
Our computer uses a stack internally called the **Call Stack**.

Example: 

```
def greet(name):
    print "hello, " + name + "!"
    greet2(name)
    print "getting ready to say bye..."
    bye()
```
This function calls 2 other functions:

```
def greet2(name):
    print "how are you, " + name + "?"
```
```
def bye():
    print "ok bye!"
```
Visually the above code is implemented:


1. ![Greet Function() called](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/g6aq6hokkwaytd32li1c.jpg)

2. ![Greet2 Function() called](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ul3ttmkw1f3l2wy3rn0c.jpg)

3. ![Greet2 is executed & then poped](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/2jsxk3odtr5nnla6p1vb.jpg)

4. ![Bye Function() is called](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xszf3wol21qqwceiiv9p.jpg)

5. ![Bye is executed & then poped](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/drt4s4cdj6br6fe6ynq6.jpg)

Explaination: 

- Firstly Greet Function is called
- Secondly Greet2 is called
- Greet2 is executed and poped
- Bye Function is called
- Bye is executed and poped
- In the end, Greet is returned too as there's nothing else to be done.

## The Call Stack with Recursion

Explained by an Example - Factorial of a Number

The Code for Factorial :-

```
def fact(x):
 if x==1:
  return 1
 else:
  return x * fact(x-1)
```

![Factorial - Recursive Function implemented using a call stack](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/xpm21d98z7wt2aiotgef.jpg)

**NOTE:**

- Using Stack is convenient but there's a cost; saving all that info can take up a lot of memory. Your Stack becomes too tall!

- It can be solved using 1. Loops instead or 2. Tail Recursion

- Suppose we write a recursive function that runs forever, then the program will run out of space & it will exit with a **Stack-Overflow Error**.


