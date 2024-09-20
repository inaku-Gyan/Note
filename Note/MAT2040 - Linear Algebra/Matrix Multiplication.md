There are several ways to multiply matrices.
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

## In Terms of **Rows**
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



