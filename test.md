# Assignment 1A - Kinematics Review and Refresher - Solutions

## Problem 1

Consider any two physical vectors, $\vec{a}$ and $\vec{b}$.  The components of each physical vector can be described in one of two reference frames.  Using the vectrix notation, we would say, $\vec{a}=\vec{\mathcal{F}}^T_1a_1 = \vec{\mathcal{F}}^T_2 a_2$ and $\vec{b}=\vec{\mathcal{F}}^T_1 b_1 = \vec{\mathcal{F}}^T_2 b_2$.  Furthermore, we can define the inner product, or dot product as, $\vec{a} \cdot \vec{b} =a_1^T b_1 =a_2^T b_2$.  Now, define a physical vector $\vec{c}=\vec{\mathcal{F}}^T_1 M_1b_1 =\vec{\mathcal{F}}^T_2 M_2b_2$. Use the inner product definition to show for any square matrix, the matrix transformation from $\mathcal{F}_1$ to $\mathcal{F}_2$ is given by $M_2 = C_{21}M_1C_{21}^T$ where $C_{21}$ is the frame rotation relating $\mathcal{F}_1$ and $\mathcal{F}_2$.  Hint, start with $\vec{a} \cdot \vec{c} =a_1^T c_1 =a_1^T M_1 b_1$.

### Solution

Starting with $\vec{a} \cdot \vec{c} =a_1^T c_1 =a_1^T M_1 b_1$ and utilizing the fact that the inner product of two vecotrs is the same regardless of the reference frame used, we get,

$\vec{a} \cdot \vec{c} =a_1^T c_1 =a_1^T M_1 b_1 = a_2^T c_2 =a_2^T M_2 b_2$.

Now use the fact, $a_2 = C_{21}a_1$ and $b_2=C_{21}b_1$, we get,

$a_1^T M_1 b_1 = (C_{21}a_1)^T M_2 (C_{21}b_1) = a_1^T C_{21}^TM_2C_{21}b_1$

Therefore, $M_1 = C_{21}^TM_2C_{21}$.  Solving for $M_2$ and using the fact that, $C_{21}^T = C_{21}^{-1}$, we get,

$M_2 = C_{21}M_1C_{21}^T$

QED $\square$

## Problem 2

Ok, let's work out the Alias vs. Alibi issue.  Start with a physical vector $\vec{r}=\vec{\mathcal{F}}^T_1 r = \vec{\mathcal{F}}^T_1\begin{bmatrix} 0.6 \\ 0.8 \\ 0\end{bmatrix}$.  Now, apply the rotation matrix $C_z(30^\circ)$ to the component vector $r$.  Given the result of the matrix operation, and the fact the we apply rotations in the positive sense using the __right-hand rule__, what is the geometric interpretation of the rotation?  How can you justify the new components?  Is the rotation Alias or Alibi?  Draw the appropriate picture.

Now, apply the rotation matrix $C_z(-30^\circ)=C_z(30^\circ)^T$ (i.e. $C_z(-30^\circ)C_z(30^\circ)^T=\mathbb{1}$) to the component vector $r$.  Same question, given the result of the matrix operation, and the fact the we apply rotations in the positive sense using the __right-hand rule__, what is the geometric interpretation of the rotation?  How can you justify the new components?  Is it Alias or Alibi?  Draw the appropriate picture.

### Solution

## Problem 3

Show that $\vec{F}_1\cdot \vec{F}_1^T=\mathbb{1}$

### Solution

Start with the definition of the Vectrix.

$\vec{\mathcal{F}_1}=\begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix}$ and $\vec{\mathcal{F}^T_1}=\begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix}$

$\Rightarrow \vec{\mathcal{F}_1} \cdot \vec{\mathcal{F}^T_1} =\begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix} \cdot\begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix}$
$=\begin{bmatrix} \vec{x}_1 \cdot \vec{x}_1 & \vec{x}_1 \cdot \vec{y}_1 & \vec{x}_1 \cdot \vec{z}_1 \\ \vec{y}_1 \cdot \vec{x}_1 & \vec{y}_1 \cdot \vec{y}_1 & \vec{y}_1 \cdot \vec{z}_1 \\ \vec{z}_1 \cdot \vec{x}_1 & \vec{z}_1 \cdot \vec{y}_1 & \vec{z}_1 \cdot \vec{z}_1 \end{bmatrix}$

Regardless of basis used, the physical vectors of the vectrix are orthonormal, or, $\vec{x}_1 \cdot \vec{x}_1 = |\vec{x}_1| = 1$ (same for $\vec{y}_1$ and $\vec{z}_1$).  Likewise,

$\vec{x}_1 \perp \vec{y}_1 \Rightarrow \vec{x}_1 \cdot \vec{y}_1 = 0$,

$\vec{x}_1 \perp \vec{z}_1 \Rightarrow \vec{x}_1 \cdot \vec{z}_1 = 0$,

$\vec{y}_1 \perp \vec{z}_1 \Rightarrow \vec{y}_1 \cdot \vec{z}_1 = 0.$

Therefore,

$\vec{\mathcal{F}_1} \cdot \vec{\mathcal{F}^T_1} =\begin{bmatrix} 1 & 0 & 0 \\ 0 & 1 & 0 \\ 0 & 0 & 1\end{bmatrix}= 1$

QED $\square$

## Problem 4

With the quaternion defined as $q=\eta+\epsilon=\cos\frac{\phi}{2}+a\cdot\sin\frac{\phi}{2}$ with $\epsilon = \begin{bmatrix} \epsilon_1 \\ \epsilon_2 \\ \epsilon_3 \end{bmatrix}$ and $a = \begin{bmatrix} a_1 \\ a_2 \\ a_3 \end{bmatrix}$, show, $|q|=1$ if $|a|=1$

### Soution

By definition, $|q| = \sqrt{\eta^2 + \epsilon^T\epsilon}$.

Now, $\epsilon^T\epsilon = \begin{bmatrix} \epsilon_1 & \epsilon_2 & \epsilon_3 \end{bmatrix} \begin{bmatrix} \epsilon_1 \\ \epsilon_2 \\ \epsilon_3 \end{bmatrix} = \epsilon_1^2 + \epsilon_2^2 + \epsilon_3^2$
$=(a_1^2 + a_2^2 + a_3^2)\sin^2{\frac{\theta}{2}}$,

where, $|a|=\sqrt{a_1^2 + a_2^2 + a_3^2}=1$.

$\Rightarrow \epsilon^T\epsilon=\sin^2{\frac{\theta}{2}}$,

$\Rightarrow |q| = \sqrt{\cos^2{\frac{\theta}{2}} + \sin^2{\frac{\theta}{2}}} = 1$

QED $\square$

## Problem #5

Show that the rotation matrix or (Direction Cosine Matrix, or DCM) is an orthonormal matrix operator, i.e., $CC^T=C^TC=1$.  (Hint:  Can you use the outer or inner product to simplify the problem?)

### Solution

By definition, $C=\vec{\mathcal{F}}_2 \cdot \vec{\mathcal{F}}_1^T$

$= \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix}$

$\Rightarrow C = \begin{bmatrix} \vec{x}_2 \cdot \vec{x}_1 & \vec{x}_2 \cdot \vec{y}_1 & \vec{x}_2 \cdot \vec{z}_1 \\ \vec{y}_2 \cdot \vec{x}_1 & \vec{y}_2 \cdot \vec{y}_1 & \vec{y}_2 \cdot \vec{z}_1 \\ \vec{z}_2 \cdot \vec{x}_1 & \vec{z}_2 \cdot \vec{y}_1 & \vec{z}_2 \cdot \vec{z}_1 \end{bmatrix}$

Notice the colums of the matrix $C$ are the basis vectors in the $\mathcal{F}_1$ frame expressed in the $\mathcal{F}_2$ frame.  We can write this as,

$C = \begin{bmatrix} x_{1,2} & y_{1,2} & z_{1,2}\end{bmatrix}$

Therefore,

$C^TC = \begin{bmatrix} x_{1,2}^T \\ y^T_{1,2} \\ z^T_{1,2}\end{bmatrix}\begin{bmatrix} x^T_{1,2} & y^T_{1,2} & z^T_{1,2}\end{bmatrix}$

$= \begin{bmatrix}
x_{1,2}^T x_{1,2} & x_{1,2}^T y_{1,2} & x_{1,2}^T z_{1,2} \\
y_{1,2}^T x_{1,2} & y_{1,2}^T y_{1,2} & y_{1,2}^T z_{1,2} \\
z_{1,2}^T x_{1,2} & z_{1,2}^T y_{1,2} & z_{1,2}^T z_{1,2} 
\end{bmatrix}$

Notice, the component vectors $x_{1,2}$, $y_{1,2}$, and $z_{1,2}$ are still orthonormal, therefore, $x_{1,2}^Tx_{1,2}=1$, $x_{1,2}^T y_{1,2}=0$, and $x_{1,2}^T z_{1,2}=0$.  The same is true for the other elements in the above matrix.  Therefore,

$C^TC=1$

We can also write the rotation matrix as,

$C = \begin{bmatrix} x_{2,1} \\ y_{2,1} \\ z_{2,1}\end{bmatrix}$

Where each row represents the projection of the $\mathcal{F}_2$ reference frame expressed in the $\mathcal{F}_1$ frame.

Using the above approach, we get,

$CC^T = \begin{bmatrix} x_{2,1} \\ y_{2,1} \\ z_{2,1}\end{bmatrix} \begin{bmatrix} x_{2,1} & y_{2,1} & z_{2,1}\end{bmatrix} = 1$

$\Rightarrow C^TC = CC^T = 1$

QED $\square$

#### Alternative Solution 1

$C=\vec{\mathcal{F}}_2 \cdot \vec{\mathcal{F}}_1^T = \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix}$

and

$\begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} = C \begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix}$

$ \Rightarrow \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} = \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix} \begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix}$

Now, if we 'dot' multiply both sides from the right by,

$\begin{bmatrix} \vec{x}_2 & \vec{y}_2 & \vec{z}_2 \end{bmatrix}$

$\Rightarrow \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_2 & \vec{y}_2 & \vec{z}_2 \end{bmatrix} = \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix} \begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_2 & \vec{y}_2 & \vec{z}_2 \end{bmatrix}$

$\Rightarrow 1 = CC^T$

Now, $C^T = (\vec{\mathcal{F}}_2 \cdot \vec{\mathcal{F}}_1^T)^T = \vec{\mathcal{F}}_1 \cdot \vec{\mathcal{F}}_2^T = \begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix} \cdot \begin{bmatrix} \vec{x}_2 & \vec{y}_2 & \vec{z}_2 \end{bmatrix}$

and

$\begin{bmatrix} \vec{x}_1 \\ \vec{y}_1 \\ \vec{z}_1 \end{bmatrix} = C^T \begin{bmatrix} \vec{x}_2 \\ \vec{y}_2 \\ \vec{z}_2 \end{bmatrix}$

Therefore, following the same proceedure from above and 'dot' multiplying from the right by, 

$\begin{bmatrix} \vec{x}_1 & \vec{y}_1 & \vec{z}_1 \end{bmatrix}$

We get, $1 = C^TC$

$ \Rightarrow C^TC = CC^T = 1$

QED $\square$

#### Alternative Solution 2

$\vec{\mathcal{F}}_2 = C\vec{\mathcal{F}}_1$

$\Rightarrow \vec{\mathcal{F}}_2 \cdot \vec{\mathcal{F}}_2^T = C \vec{\mathcal{F}}_1 \cdot \vec{\mathcal{F}}_2^T$

$\Rightarrow 1 = CC^T$

Likewise,

$\vec{\mathcal{F}}_1 = C^T\vec{\mathcal{F}}_2$

$\Rightarrow \vec{\mathcal{F}}_1 \cdot \vec{\mathcal{F}}_1^T = C^T \vec{\mathcal{F}}_2 \cdot \vec{\mathcal{F}}_1^T$

$\Rightarrow 1 = C^TC$

$\Rightarrow C^TC = CC^T = 1$

QED $\square$

### Alternatie Solution 3

Use the fact that for arbitrary vectors a and b, we can write a_2 = C21 a1, etc...

## Problem #6

1. Use the definition of the quaternion to verify the quaternion product rule $p \odot q = \begin{bmatrix} \eta_p\epsilon_q + \eta_q\epsilon_p+\epsilon_p^\times\epsilon_q \\ \eta_p\eta_q-\epsilon_p^T\epsilon_q\end{bmatrix}$ presented in lecture.
2. Show $p\otimes q = q \odot p$.
3. In Aero 421 we defined the quaternions error as, $q_e =q_c^\ast q$ with the Hamiltonian quaternion product implied, i.e., $q_e = q_c^\ast \odot q$.  How would you define the quaternion error using the $\otimes$ operator?
4. Verify $\Xi^T(q)\Phi(q)=C_{21}$.

### Solution

#### Part 1

With, $p=\eta_p + \epsilon_p$ and $q=\eta_q + \epsilon_q$ then,

$pq = (\eta_p + \epsilon_p)(\eta_q + \epsilon_q)$

$=\eta_p\eta_q + \eta_p\epsilon_q + \eta_q\epsilon_p + \epsilon_q\epsilon_q$

Looking at the last term, we have,

$\epsilon_q\epsilon_q = ( \epsilon_{p_x}i + \epsilon_{p_x}j + \epsilon_{p_x}k)(\epsilon_{q_x}i + \epsilon_{q_x}j + \epsilon_{q_x}k)$

$= \epsilon_{p_x}\epsilon_{q_x}i^2 + \epsilon_{p_x}\epsilon_{q_y}ij +\epsilon_{p_x}\epsilon_{q_z}ik +\epsilon_{p_y}\epsilon_{q_x}ji +\epsilon_{p_y}\epsilon_{q_y}j^2 +\epsilon_{p_y}\epsilon_{q_z}jk+\epsilon_{p_z}\epsilon_{q_x}ki+\epsilon_{p_z}\epsilon_{q_y}kj+\epsilon_{p_z}\epsilon_{q_z}k^2$

Using the Hamiltonian relationships, 

$i^2=j^2=k^2=ijk=-1$

(which results in the Right Hand Rule _RHR_)

$ij=k, jk=i, ki=j$

we have,

$\epsilon_q\epsilon_q = -[\epsilon_{p_x}\epsilon_{q_x}+\epsilon_{p_y}\epsilon_{q_y}+\epsilon_{p_z}\epsilon_{q_z}]+
(\epsilon_{p_y}\epsilon_{q_z} - \epsilon_{p_z}\epsilon_{q_y})i + 
(\epsilon_{p_z}\epsilon_{q_x} - \epsilon_{p_x}\epsilon_{q_z})j + 
(\epsilon_{p_x}\epsilon_{q_y} - \epsilon_{p_y}\epsilon_{q_x})k$

Notice,

$\epsilon_{p_x}\epsilon_{q_x}+\epsilon_{p_y}\epsilon_{q_y}+\epsilon_{p_z}\epsilon_{q_z} = \epsilon_p^T\epsilon_q$

and

$(\epsilon_{p_y}\epsilon_{q_z} - \epsilon_{p_z}\epsilon_{q_y})i + (\epsilon_{p_z}\epsilon_{q_x} - \epsilon_{p_x}\epsilon_{q_z})j + (\epsilon_{p_x}\epsilon_{q_y} - \epsilon_{p_y}\epsilon_{q_x})k = \epsilon_p^\times \epsilon_q$

$\Rightarrow pq = \eta_p\eta_q - \epsilon_p^T\epsilon_q + \eta_p\epsilon_q + \eta_q\epsilon_p +\epsilon_p^\times \epsilon_q$

QED $\square$

#### Part 2.

Since $p \odot q = \begin{bmatrix} \eta_p\epsilon_q + \eta_q\epsilon_p+\epsilon_p^\times\epsilon_q \\ \eta_p\eta_q-\epsilon_p^T\epsilon_q\end{bmatrix}$

and 

$p \otimes q = \begin{bmatrix} \eta_p\epsilon_q + \eta_q\epsilon_p - \epsilon_p^\times\epsilon_q \\ \eta_p\eta_q-\epsilon_p^T\epsilon_q\end{bmatrix}$

$\Rightarrow q \odot p = \begin{bmatrix} \eta_q\epsilon_p + \eta_p\epsilon_q+\epsilon_q^\times\epsilon_p \\ \eta_q\eta_p-\epsilon_q^T\epsilon_p\end{bmatrix}$

Since the real/vector parts commute under multiplication, and $\epsilon_q^T\epsilon_p = \epsilon_p^T\epsilon_q$ and $\epsilon_q^\times\epsilon_p = - \epsilon_p^\times\epsilon_q$

$\Rightarrow q \odot p = \begin{bmatrix} \eta_p\epsilon_q + \eta_q\epsilon_p - \epsilon_p^\times\epsilon_q \\ \eta_p\eta_q-\epsilon_p^T\epsilon_q\end{bmatrix}$

$\therefore p \otimes q = q \odot p$

QED $\square$

#### Part 3

As defined in Aero 421, $q_e = q_c^\ast \odot q$.  Using the result from part 2, we can switch the order and chage the operator, so, $q_e = q \otimes q_c^\ast$

#### Part 4

Verify $\Xi^T(q)\Phi(q)=C_{21}$

Well, $\Xi(q) = \begin{bmatrix} \eta\mathbb{1}+\epsilon^\times \\ -\epsilon^T \end{bmatrix}$ and $\Phi(q) = \begin{bmatrix} \eta\mathbb{1}-\epsilon^\times \\ -\epsilon^T  \end{bmatrix}$

$\Rightarrow \Xi^T(q)=\begin{bmatrix} \eta\mathbb{1}^T+(\epsilon^\times)^T && (-\epsilon^T)^T \end{bmatrix}=
\begin{bmatrix} \eta\mathbb{1} - \epsilon^\times && -\epsilon \end{bmatrix}$

$\Rightarrow \Xi^T(q) \Phi(q)= \begin{bmatrix} \eta\mathbb{1}-\epsilon^\times && -\epsilon \end{bmatrix} \begin{bmatrix} \eta\mathbb{1}-\epsilon^\times \\ -\epsilon^T  \end{bmatrix}$

$=\eta^2\mathbb{1} - \eta\epsilon^\times - \eta\epsilon^\times + \epsilon^\times\epsilon^\times + \epsilon\epsilon^T$

Now use the identity $\epsilon^\times\epsilon^\times = -\epsilon^T\epsilon \mathbb{1} + \epsilon \epsilon^T$

$\Rightarrow \Xi^T(q) \Phi(q) = \eta^2\mathbb{1} - \eta\epsilon^\times - \eta\epsilon^\times + -\epsilon^T\epsilon \mathbb{1} + \epsilon \epsilon^T + \epsilon\epsilon^T$

$=(\eta^2 -\epsilon^T\epsilon) \mathbb{1} + 2\epsilon \epsilon^T - 2\eta\epsilon^\times$

Now, since $|q|^2 = 1 = \eta^2 + \epsilon^T\epsilon$ $\Rightarrow \epsilon^T\epsilon = 1 - \eta^2$

$\Rightarrow \Xi^T(q) \Phi(q) = (2\eta^2 -1) \mathbb{1} + 2\epsilon \epsilon^T - 2\eta\epsilon^\times =C_{21}$ based on the _Mehiel Kinematic Quad Chart_.

QED $\square$

## Other Problems

Show $(\epsilon^T r_2)\epsilon = (\epsilon\epsilon^T)r_2$

### Solution:

The easiest method is to use matrix multiplication identiies.

Notice, $(\epsilon^T r_2)\epsilon = \epsilon(\epsilon^T r_2)$ since $\epsilon^T r_2$ is a scalar.  And, $\epsilon(\epsilon^T r_2) = (\epsilon\epsilon^T )r_2$ since vector multiplication is associative.

$\Rightarrow (\epsilon^T r_2)\epsilon = (\epsilon\epsilon^T)r_2$

You can also show this relationship is true by multiplying all terms out.
