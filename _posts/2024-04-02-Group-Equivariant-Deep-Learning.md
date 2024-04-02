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
