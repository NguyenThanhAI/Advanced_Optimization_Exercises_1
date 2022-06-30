### 2 Cho hàm số $f(x, y) = x^4 + x^2 - 6xy + 3y^2$. Hãy tìm các điểm cực trị địa phương của $f$, hãy chỉ rõ đó là cực đại hay cực tiểu địa phương

$$f(x, y) = x^4 + x^2 - 6xy + 3y^2$$

Ta có $\mathrm{dom}(f)=\mathbb{R}^2$ là một tập lồi

$$\nabla f(x, y) = \begin{bmatrix} \dfrac{\partial f(x, y)}{\partial x} \\ \dfrac{\partial f(x, y)}{\partial y}\end{bmatrix} = \begin{bmatrix} 4x^3 + 2x - 6y \\ -6x + 6y \end{bmatrix}$$

$$\nabla^2 f(x,y)=\begin{bmatrix} \dfrac{\partial^2 f(x, y)}{\partial x^2} & \dfrac{\partial^2 f(x, y)}{\partial x\partial y} \\ \dfrac{\partial^2 f(x, y)}{\partial y \partial x } & \dfrac{\partial^2 f(x, y)}{\partial y^2 } \end{bmatrix}=\begin{bmatrix} 12x^2 + 2 & -6 \\ -6 & 6 \end{bmatrix}$$

Ta xét:


$$\det(\begin{bmatrix} 12x^2 + 2  \end{bmatrix})>0 \thickspace \forall (x, y) \in \mathbb{R}^2$$

$$\det(\nabla^2 f(x,y))=\det\Bigg(\begin{bmatrix} 12x^2 + 2 & -6 \\ -6 & 6 \end{bmatrix} \Bigg)=6(12x^2 + 2) - 36 =72x^2 - 24$$

- $\det(\nabla^2 f(x,y)) < 0$ với $x \in \Big(-\dfrac{1}{\sqrt{3}}; \dfrac{1}{\sqrt{3}}\Big)$, $\nabla^2 f(x,y))$ là ma trận xác định âm.

- $\det(\nabla^2 f(x,y)) > 0$ với $x \in \Big(-\infty;-\dfrac{1}{\sqrt{3}}\Big) \cup \Big(\dfrac{1}{\sqrt{3}}; +\infty\Big)$, $\nabla^2 f(x,y))$ là ma trận xác định dương

Như vậy $\nabla^2 f(x,y))$ là ma trận không xác định dấu do $\nabla^2 f(x,y)) \succ 0$ hay $\nabla^2 f(x,y)) \prec 0$ phụ thuộc vào giá trị $x$.

Để tìm điểm dừng, ta giải phương trình $\nabla f(x, y) = \bold{0}$

$$\nabla f(x, y) = \begin{bmatrix} 4x^3 + 2x - 6y \\ -6x + 6y \end{bmatrix} = \begin{bmatrix} 0 \\ 0 \end{bmatrix}$$

$$\Leftrightarrow \begin{cases} 4x^3 + 2x - 6y = 0 \\ x = y \end{cases} \Leftrightarrow \begin{cases} 4x^3 + 2x - 6x = 0 \\ x = y \end{cases}$$

$$\Leftrightarrow \begin{cases} 4x(x^2-1) = 0 \\ x = y \end{cases}$$

$$x=y=0, x=y=1,x=y=-1$$

$\left[\begin{array}{l} \end{array}\right$


- $\nabla^2 f(0,0))=\begin{bmatrix} 2 & -6 \\ -6 & 6 \end{bmatrix}$. Ta có $\det(\begin{bmatrix}2\end{bmatrix})=2>0, \det{\Big(\begin{bmatrix} 2 & -6 \\ -6 & 6 \end{bmatrix}\Big)}=2\times6 - (-6)\times(-6)=-24<0$. $\nabla^2 f(0,0))$ là ma trận xác định âm. Vậy $x=y=0$ là một điểm cực đại địa phương.

- $\nabla^2 f(1,1)=\begin{bmatrix} 14 & -6 \\ -6 & 6 \end{bmatrix}$. $\det{(\begin{bmatrix}14\end{bmatrix})}=14>0, \det{\Big(\begin{bmatrix} 14 & -6 \\ -6 & 6 \end{bmatrix}\Big)}=14\times6 - (-6)\times(-6)=48>0$.$\nabla^2 f(1,1)$ là ma trận xác định dương. Vậy $x=y=1$ là một cực tiểu địa phương.

- $\nabla^2 f(-1,-1)=\begin{bmatrix} 14 & -6 \\ -6 & 6 \end{bmatrix}$. $\det{(\begin{bmatrix}14\end{bmatrix})}=14>0, \det{\Big(\begin{bmatrix} 14 & -6 \\ -6 & 6 \end{bmatrix}\Big)}=14\times6 - (-6)\times(-6)=48>0$.$\nabla^2 f(-1,-1)$ là ma trận xác định dương. Vậy $x=y=-1$ là một cực tiểu địa phương.

Ta có 
$$\lim_{\substack{x \rightarrow +\infty\\y \rightarrow+\infty}}f(x, y)=\lim_{\substack{x \rightarrow +\infty\\y \rightarrow-\infty}}f(x, y)
=\lim_{\substack{x \rightarrow -\infty\\y \rightarrow+\infty}}f(x, y)
=\lim_{\substack{x \rightarrow -\infty\\y \rightarrow-\infty}}f(x, y)=+\infty$$

Nên $x=y=0$ là một cực đại địa phương

$f(1,1)=f(-1,-1)=-1<f(x,y) \thickspace \forall (x,y) \in \mathbb{R}^2 \backslash \lbrace (1, 1), (-1, -1) \rbrace$

Nên $x=y=1$ và $x=y=-1$ là các cực tiểu toàn cục