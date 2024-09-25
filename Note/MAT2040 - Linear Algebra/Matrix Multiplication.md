There are several ways to multiply two matrices.
Suppose $AB=C$, where $A\in\mathbb{R}^{m\times p}, B\in\mathbb{R}^{p\times n}, C\in\mathbb{R}^{m\times n}$.

## Entries
Each entry of $C$ is the dot product of the corresponding row of $A$ and column of $B$.
$$
c_{ij} = \vec{\mathbf{a}}_i\cdot\mathbf{b}_j = \sum^{p}_{k=1}a_{ik}b_{kj}
$$
$$
\begin{bmatrix}
 * &  &  &  &  & \\
 a_{i1} & a_{i2} &  & \cdots  &  & a_{ip}\\
 * &  &  &  &  & \\
 * &  &  &  &  &
\end{bmatrix}
\begin{bmatrix}
 * & * & * & b_{1j} & *\\
  &  &  & b_{2j} & \\
  &  &  &  & \\
  &  &  & \vdots  &\\
  &  &  &  &\\
  &  &  & b_{pj} &
\end{bmatrix}=
\begin{bmatrix}
  &  &  & * & \\
 * & * & * & c_{ij} & * \\
  &  &  & * & \\
  &  &  & * & \\
\end{bmatrix}
$$
^b0dd59

## Columns
Each column of $C$ is a linear combination of the columns of $A$.
$$
\mathbf{c}_j=A\cdot\mathbf{b}_j=\sum^{p}_{k=1}b_{kj}\mathbf{a}_k
$$
$$
\begin{bmatrix}
\mid&\mid&&\mid\\
\mathbf{a}_1&\mathbf{a}_2&\cdots&\mathbf{a}_p
\\\mid&\mid&&\mid
\end{bmatrix}
\begin{bmatrix}b_{1j}\\b_{2j}\\\vdots\\b_{pj}\end{bmatrix}=
\begin{bmatrix}
\mid\\
\mathbf{c}_j
\\\mid
\end{bmatrix}
$$

## Rows
Each row of $C$ is a linear combination of the rows of $B$.
$$
\vec{\mathbf{c}}_i=\vec{\mathbf{a}}_i\cdot B=\sum^{p}_{k=1}a_{ik}\vec{\mathbf{b}}_k
$$
$$
\begin{pmatrix}a_{i1}&a_{i2}&\cdots&a_{ip}\end{pmatrix}
\begin{bmatrix}
\ -&\vec{\mathbf{b}}_1&-\ \\
\ -&\vec{\mathbf{b}}_2&-\ \\
&\vdots&\\
\ -&\vec{\mathbf{b}}_p&-\ 
\end{bmatrix}=
\begin{pmatrix}\ -&\vec{\mathbf{c}}_{i}&-\ \end{pmatrix}
$$

## Block Multiplication
It is possible to partition $A$ and $B$ into submatrices and complete the product, if and only if the number of columns into which $A$ is partitioned is equal to the number of rows into which $B$ is partitioned, and that the number of columns in the submatrices of the $q$-th column in $A$ is equal to the number of rows in the submatrices of the $q$-th row in $B$.

$$
\left[
\begin{array}{cc|c|ccc|c|c} 
\# & \# & @ & \# & \# & \# & @ & \# \\
* & * & * & * & * & * & * & * \\
* & * & * & * & * & * & * & * \\ \hdashline
* & * & * & * & * & * & * & * \\
* & * & * & * & * & * & * & * \\
\end{array}
\right]
\left[
\begin{array}{cc:c:c} 
\# & * & * & * \\
\# & * & * & * \\ \hline 
@ & * & * & * \\ \hline 
\# & * & * & * \\
\# & * & * & * \\
\# & * & * & * \\ \hline 
@ & * & * & * \\ \hline 
\# & * & * & * \\
\end{array}
\right]=
\left[
\begin{array}{cc:c:ccc} 
* & * & * & * \\
* & * & * & * \\
* & * & * & * \\ \hdashline 
* & * & * & * \\
* & * & * & * \\
\end{array}
\right]
$$


## Properties

#### Interactions between $A$ and $B$
During the entire operation, $a_{ik}$ will complete exactly $n$ multiplications, which are with $b_{k1}, b_{k2}, ..., b_{kn}$ respectively; and $b_{kj}$ will complete exactly $m$ multiplications, which are with $a_{1k}, a_{2k}, ..., a_{mk}$ respectively.

#### Effects on $C$
- An item of the $i$-th row of $A$ will exactly affect the whole $i$-th row of $C$.
- An item of the $j$-th column of $B$ will exactly affect the whole $j$-th column of $C$.

