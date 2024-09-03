+++
title = 'Proving 1 > 0'
date = 2018-12-10
draft = false
[params]
  math = true
+++


> This post was first published in my old blog, hosted at `blog.neerajadhikari.com.np`.
> I have since taken down the old blog and copied some of its posts here.

How do you know that 1 is greater than 0? What a silly question! By intuition,
you might say. Zero means nothing, and one means a unit quantity of something.
And surely something is more than nothing. Something even an infant would know.
But that's intuition, or common sense. Intuition is a powerful thing, but it
won't get us very far in mathematics. That's why we have mathematical rigor -
where we use axiomatic systems which have a set of statements that we consider
true (axioms), and then use rigid, very mechanical symbol-manipulation rules to
generate other statements that are true.

I am currently studying Michael Spivak's *Calculus*, both to brush up my
calculus knowledge and because it is known for taking a very rigorous approach,
meticulously proving theorems that other books often state without proof. The
first chapter is on the properties of numbers. While it doesn't start right
from the [bottom](https://en.wikipedia.org/wiki/Peano_axioms) (it leaves out
properties of equality, for example), it presents of 12 properties from which
we can derive other interesting truths. If we assume just some basic properties
of addition, multiplication and the inequality symbols, and know nothing else
about numbers except what our properties and derived facts tell us, lets see
what we need to conclude that $$ 1 > 0 $$.

Here are the 12 properties that we will consider true:

### &nbsp;&nbsp;&nbsp;&nbsp;Addition Properties

1.  If $$a$$, $$b$$ and $$c$$ are any numbers,

    $$$ a + (b + c) = (a + b) + c $$$

    This property is called the *associativity of addition* and it provides us
    a means of adding more than two numbers, by saying that the order in which
    you perform the individual additions does not matter.

2.  If $$a$$ is any number,

    $$$ a + 0 = 0 + a = a $$$

    This property states the existence of the number 0, indicates its defining
    behavior. 0 is called the *additive identity* because it leaves numbers
    unchanged when it is added to them. With this property have our first
    actual, concrete number. The previous property talked of 'any numbers' and
    used letters to denote them but provided no examples.

3.  For every number $$a$$, there is a number $$-a$$ such that

    $$$ a + (-a) = (-a) + a = 0 $$$
 
    Here we establish a relationship between any (and every) number, its
    *additive inverse* that we denote by a minus sign before the number, and 0.
    For convenience, we can write $$a+(-b)$$ as $$a-b$$.

4.  If $$a$$ and $$b$$ are any numbers, then

    $$$ a + b = b + a $$$

    Essentially, the result of addition is the same, whatever the order of
    numbers around the addition symbol. This property is known as the
    *commutativity of addition*.
    
    ### Multiplication Properties

5.  If $$a$$, $$b$$ and $$c$$ are any numbers,
    
    $$$ a \cdot (b \cdot c)  = (a \cdot b) \cdot c $$$

    This is the same as property 1, but for a new operation we call
    multiplication and denote by $$\cdot$$. This is called the *associativity
    of multiplication*.

6.  If $$a$$ is any number,
    
    $$$
    \begin{eqnarray}
    a \cdot 1  = 1 \cdot a = a\\
 Also, 1 \neq 0
    \end{eqnarray}
    $$$

    Like property 2 does for addition, this property defines a *multiplicative
    identity*. Muliply any number with $$1$$, and you leave the number unchanged.
    The property also mentions that $$1 \neq 0$$, to differentiate the new
    concrete number $$1$$ that we have introduced here from the $$0$$ that we
    introduced earlier. Without this disclaimer, $$1$$ could have been just
    another symbol for $$0$$. There is nothing in the previous properties to
    prohibit that, because this is the property that defines $$1$$ for the
    first time. 
     
7.  For every number $$a \neq 0$$, there exists a number $$a^{-1}$$ such that

    $$$ a \cdot a^{-1} = a^{-1} \cdot a = 1 $$$

    Similar to property 3, but this one defines a *multiplicative inverse*. And
    a very important thing to note, multiplicative inverses are defined for all
    numbers except $$0$$.

8.  If $$a$$ and $$b$$ are any numbers,
    
    $$$ a \cdot b = b \cdot a $$$

    Like for addition, the order of the numbers you are multiplying does not
    affect the result of multiplication. This is called the *commutativity of
    multiplication*.

    At the moment we know a lot about addition and multiplication, but there is
    not much we can do. For example, we would be helpless if we wanted to prove
    that $$ a \cdot 0 = 0 $$ for any number a. That is because in the
    properties we have seen, $$0$$ only appears with addition and what we are
    trying to prove involves multiplication. So we need something that relates
    these two operations.

    ### A Property of Both

9.  If $$a$$, $$b$$ and $$c$$ are any numbers,
    
    $$$ a \cdot (b+c) = a \cdot b + a \cdot c $$$

    This is called the *distributive law*, and by tying addition and
    multiplication together it enables us to prove what we want:

    $$$
    \begin{eqnarray}
        a \cdot 0 + a \cdot 0 &=& a \cdot (0 + 0) \nonumber \\
        &=& a \cdot 0 \nonumber \\
    \end{eqnarray}
    $$$

    Adding $$-(a\cdot0)$$ to both sides, we get $$ \mathbf{a \cdot 0= 0}$$

    While we are here, lets prove two other facts we will need later. First,
    $$ (-a) \cdot b = -(a \cdot b)$$, which is simple:

    $$$
    \begin{eqnarray}
        (-a) \cdot b + a \cdot b &=& [(-a) + a] \cdot b \nonumber \\
        &=& 0 \cdot b \nonumber \\
        &=& 0 \nonumber \\
    \end{eqnarray}
    $$$

    Adding $$-(a \cdot b)$$ to both sides, we get
    $$\mathbf{(-a) \cdot b = -(a\cdot b)}$$

    Another fact we can prove is $$(-a)\cdot(-b) = a\cdot b$$

    $$$
    \begin{eqnarray}
        (-a) \cdot (-b) + [- (a \cdot b)] &=& (-a) \cdot (-b) + (-a) \cdot b \nonumber \\
        &=& (-a) \cdot [(-b) + b] \nonumber \\
        &=& (-a) \cdot 0 \nonumber \\
        &=& 0 \nonumber \\
    \end{eqnarray}
    $$$

    Adding $$a \cdot b$$ to both sides, we get
    $$\mathbf{(-a) \cdot (-b) = (a\cdot b)}$$

    A good set of facts we've got proved at the point, but absolutely no way of
    doing anything with inequalities. Essentially, we know there are *at least*
    two numbers, $$0$$ and $$1$$, but have no notion of 'greater than' or
    'smaller than'. The next three properties will change this situation.
    
    Instead of defining inequalities right away, it is more convenient to
    define $$P$$ as the set of all positve numbers, and state properties 10-12
    in terms of $$P$$.

    ### Inequality Properties

10. If $$a$$ is any number, then one and only one of the following is true:
    - $$ a = 0 $$
    - $$ a $$ is in $$P$$
    - $$ (-a) $$ is in $$P$$

    This is called the *Trichotomy Law*. It cleanly separates numbers into
    three categories: $$0$$, numbers which are in $$P$$ and numbers whose
    additive inverses are in $$P$$.

11. If $$a$$ and $$b$$ are in $$P$$, then $$a + b$$ is in $$P$$.

    This is called the *closure of positive numbers under addition*.

12. If $$a$$ and $$b$$ are in $$P$$, then $$a \cdot b$$ is in $$P$$.

    This is called the *closure of positive numbers under
    multiplication*.

So now we have our 12 properties. It is time now to define the symbols $$\lt$$, 
$$\gt$$, $$\le$$ and $$\ge$$.

$$$
\begin{eqnarray}
a \gt b & \; \text{if} \; & a - b \; \text{is in} \; P \\
a \lt b & \; \text{if} \; & b \gt a\\
a \ge b & \; \text{if} \; & a \gt b \; \text{or} \; a = b\\
a \le b & \; \text{if} \; & a \lt b \; \text{or} \; a = b\\
\end{eqnarray}
$$$


Hold on, because we are almost there. We need to prove one crucial fact first:
that if $$ a \lt 0 $$ and $$ b \lt 0 $$, then $$ a \cdot b \gt 0 $$. In other
words, the product of two negative numbers is positive.

$$$
\begin{eqnarray}
& \Rightarrow & a \lt 0 \\
& \Rightarrow & 0 \gt a \\
& \Rightarrow & 0 \gt a \\
& \Rightarrow & 0-a \; \text{is in} \; P\\
& \Rightarrow & -a \; \text{is in} \; P\\
& \text{Similarly,} & -b \; \text{is in} \; P\\
& \Rightarrow & (-a)\cdot(-b) \; \text{is in} \; P\\
& \Rightarrow & a\cdot b \; \text{is in} \; P\\
& \Rightarrow & a\cdot b - 0\; \text{is in} \; P\\
& \Rightarrow & \mathbf{a\cdot b \gt 0}\\
& \end{eqnarray}
$$$

We have proved that if $$ a \lt 0 $$ and $$ b \lt 0 $$, then
$$ a \cdot b \gt 0 $$. But it is also true that $$ a \cdot b \gt 0 $$ when
$$ a \gt 0 $$ and $$ b \gt 0 $$, because in that case both $$a$$ and $$b$$ are
in $$P$$ and thus $$a\cdot b$$ is in $$P$$ by Property 12. To say them both in
the same sentence, $$ a \cdot b \gt 0 $$ when $$ a \lt 0 $$ and $$ b \lt 0 $$
or $$ a \gt 0 $$ and $$ b \gt 0 $$. In the special case where $$a=b$$,
$$a^2\gt0$$ when $$a \gt 0$$ or $$a \lt 0$$. By the trichotomy law, that is the
same as $$a \neq 0$$. And because we have defined $$1$$ as being not equal to
$$0$$, and because $$ 1^2 = 1\cdot1 = 1$$, we can finally conclude what we
needed to:

$$$ \mathbf{1 \gt 0} $$$

### P.S.

It took a lot of properties to prove that $$1 \gt 0$$, but after proving just
two more facts, we can proceed to prove inequality relations for all integers.

If $$a\lt b$$, so $$b-a$$ is in $$P$$, then
$$(b-a)+(c-c) = (b+c) - (a+c)$$ is in $$P$$. Thus, $$a+c \lt b+c$$.

If $$a\lt b$$ and $$b \lt c$$, then $$b-a$$ is in $$P$$ and $$c-b$$ is in
$$P$$. By Property 11, $$(c-b)+(b-a) = c-a$$ is in $$P$$. Thus, $$ a \lt c$$.

Because we have $$ 0 \lt 1$$, by the former of these two facts,
$$ 0 + 1 \lt 1 + 1 $$, or $$1 \lt 1 + 1$$. Instead of leaving $$ 1 + 1$$ as it
is, we can use the well-known symbol for it, $$2$$, so $$\mathbf{ 1 \lt 2}$$.
Similarly, $$1 + 1 \lt 2 + 1$$, aka $$\mathbf{2 \lt 3}$$ and so on. And we can
also compare non-consecutive numbers: becuase $$ 0 \lt 1 $$ and
$$ 1 \lt 2 $$, $$\mathbf{0 \lt 2}$$. Similarly, we can derive inequalities for
the negative numbers, and *viola!*, an order is enforced on all integers.
