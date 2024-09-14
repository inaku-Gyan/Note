There are four ways to multiply matrices.
Suppose $AB=C$, where $A\in\mathbb{R}^{m\times p}, B\in\mathbb{R}^{p\times n}, C\in\mathbb{R}^{m\times n}$.

## In Terms of **Entries**
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


## In Terms of **Columns**
Each column of $C$ is a linear combination of the columns of $A$.
$$
\mathbf{c}_j=\sum^{p}_{k=1}b_{kj}\mathbf{a}_k
$$
$$
A\begin{bmatrix}b_{11}\\b_{21}\\\vdots\\b_{p1}\end{bmatrix}+
A\begin{bmatrix}b_{12}\\b_{22}\\\vdots\\b_{p2}\end{bmatrix}+\cdots+
A\begin{bmatrix}b_{1n}\\b_{2n}\\\vdots\\b_{pn}\end{bmatrix}=
\begin{bmatrix} 
\mid &\mid &&\mid\\
\mathbf{c}_1 & \mathbf{c}_2 & \cdots & \mathbf{c}_n \\
\mid&\mid&&\mid\\\mid&\mid&&\mid\\
\end{bmatrix}
$$

## In Terms of **Rows**
Each row of $C$ is a linear combination of the rows of $B$.
$$
\vec{\mathbf{c}}_i=\sum^{p}_{k=1}a_{ik}\vec{\mathbf{b}}_k
$$





