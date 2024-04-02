## Group Equivariant Deep Learning


#### Lecture 1 : By their equivariant property G-CNNs are relevant for any type of structured data

*multi-channel functions* $f : X → R^{N_c}$ defined on some domain $X$ and with $N_c$ the number of channels.
Let $L_2(X)^{N_c}$ denote the *space of square integrable signals*.
*Scalar valued signals* are those for which $N_c = 1$, denoted with $f: X → R$.
The signal value of a multi-channel signal is a vector $f(x)$.
#### Convolution and cross-correlation
Correlations are convolutions with reflected kernels. One can think of convolutions/correlations as template matching with the kernel k acting as a tamplate movin g over the signer f at each location x. Matching occurs between the translated kernel and the underlging signel by taking the inner product. 

- template matching


- convolution commute (k*f = f*k) and correlations do not. 


Equivariance is important as you would like not to lose information when input is transformed. When presented with rotations of the same feature. 

| CNN  | G-CNN |
|------|-------|
| not rotational equivariant | rotational equivariant|
| Translation equivariant due to convolutions | Equivariance beyond translations due to group convolutions |
| ... | geometric guarantees|
| ... | increased weight sharing|
| ... | weight sharing over a larger group of transformations (not just translations). By means of tremplate matching with correlation kernels. The kernel may be translated/rotated/scaled. |
| ... | efficient representation learning by leveraging symmetries|


Feature maps are transformed by group correlations. After the first group covolution a feature map on SE(2) is obtained. Layers are parametrized by 3-dimensional kernels. 
### Definition 2.1 (Group, group product, group inverse)
A group is an algebraic structure that consists of a set $G$ and a binary operator $\cdot$ called the group product, that satisfies the following axioms:
- **Closure**: $\forall h, g \in G$ we have $h \cdot g \in G$;
- **Identity**: there exists an identity element $e \in G$;
- **Inverse**: for each $g \in G$ there exists an inverse element $g^{-1} \in G$ such that $g^{-1} \cdot g = g \cdot g^{-1} = e$; and
- **Associativity**: for each $g, h, i \in G$ we have $(g \cdot h) \cdot i = g \cdot (h \cdot i)$.


### Translation Group $G = (R^d,+)$
### Rotation Group, special ortogonal group G = SO(d)
### 2D Rotation group G = SO(2) in parametric form
### Rotation-translation group, special Euclidean motiion group SE(d)
### Discrete translation group $G = (R^d, +)$

## Group actions and representations
How groups act on vectors and functions?
- Matrix representation
- Left-regular representation

Action of G on G: a group acting on itself via the group product.
Action of G on the domain of a function X. 
Action of G on $R^d$.
Action of G on $L_s(X)$: done via left regular denoted by $L_g$.

## Homogeneous space
- Transitive action
- Semidirect product
- Coset
- Quotient space G/H. G/H is a homogeneous space of G.
- Affine group SE(2)


- group correlations,
-  roto-translation groupp SE(2)
  


- Group theory
- Regular group convolutions
- SE(2) equivariant NN
- 
#### Lecture 2
- Homogeneous spaces
- G-convs are all you need
- motivation equivaraint graph NNS
- Message passing
- Conditioning message functions
- 
