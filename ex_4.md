### 4 Xét hàm số Rosenbrock

$$f(x)=100(x_2 - x_1^2)^2 + (1-x_1)^2$$

1. $f$ có phải là hàm lồi không? Tại sao?

2. Hãy tìm tất cả các điểm cực tiểu địa phương của $f$. Hàm $f$ có điểm cực tiểu toàn cục không? Nếu có hãy chỉ ra điểm đó là điểm nào?


$$f(x)=100(x_2 - x_1^2)^2 + (1-x_1)^2$$

#### 4.1

Ta có $\mathrm{dom}(f)=\mathbb{R}^{2}$ là một tập lồi.

Ta xét:

$$\nabla f(x) = \begin{bmatrix} \dfrac{\partial f(x)}{\partial x_1} \\ \dfrac{\partial f(x)}{\partial x_2}\end{bmatrix} = \begin{bmatrix} -400x_1(x_2 - x_1^2) -2(1-x_1) \\ 200(x_2 - x_1^2) \end{bmatrix}$$

$$\nabla^2 f(x)=\begin{bmatrix} \dfrac{\partial^2 f(x)}{\partial x_1^2} & \dfrac{\partial^2 f(x)}{\partial x_1\partial x_2} \\ \dfrac{\partial^2 f(x)}{\partial x_2 \partial x_1 } & \dfrac{\partial^2 f(x)}{\partial x_2^2 } \end{bmatrix} = \begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 & -400 x_1 \\ -400x_1 & 200 \end{bmatrix}$$

Ta có:

$$\det (\begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 \end{bmatrix})=-400 x_2 + 1200x_1^2 + 2$$
Dấu của định thức này phụ thuộc vào $x_1, x_2$. Nếu $x_2 > \dfrac{1200x_1^2 + 2}{400}$ thì định thức $\det (\begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 \end{bmatrix})<0$ và nếu $x_2 < \dfrac{1200x_1^2 + 2}{400}$ thì $\det (\begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 \end{bmatrix})>0$. Hay nói cách khác ma trận $\begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 \end{bmatrix}$ là ma trận xác định dấu âm hay dương phụ thuộc vào $x_1, x_2$. $\begin{bmatrix} -400 x_2 + 1200x_1^2 + 2 \end{bmatrix}$ là ma trận không xác định dấu.


$\nabla^2 f(x)$ là ma trận không xác định dấu nên $f(x)$ không là hàm lồi

#### 4.2

Ta xét $\nabla f(x)=\bold{0}$

$$\Leftrightarrow \begin{cases} -400x_1(x_2 - x_1^2) -2(1-x_1) = 0 \\ 200(x_2 - x_1^2) = 0 \end{cases}$$

$$\Leftrightarrow \begin{cases} -400x_1(x_2 - x_1^2) -2(1-x_1) = 0 \\ x_2 = x_1^2 \end{cases}$$

$$\Leftrightarrow \begin{cases} x_1=1 \\ x_2 = x_1^2=1 \end{cases}$$

Ta xét:

$$\nabla^2 f(1, 1)=\begin{bmatrix} 802 & -400 \\ -400 & 200 \end{bmatrix}$$

$$\det(\lbrack 802 \rbrack)=802>0$$

$$\det{\Big(\begin{bmatrix} 802 & -400 \\ -400 & 200 \end{bmatrix} \Big)}=802\times200 - (-400)\times(-400)=400>0$$

$$\Rightarrow\nabla^2 f(1, 1) \succ 0$$

Vậy $x_1=x_2=1$ là một cực tiểu địa phương

$f(1, 1)=0$ và $f(x_1, x_2) \geq 0=f(1,1) \thickspace \forall (x_1, x_2) \in \mathbb{R}^2$ nên $x_1=x_2=1$ là cực tiểu toàn cục.

Ta có 
$$\lim_{\substack{x_1 \rightarrow +\infty\\x_2 \rightarrow+\infty}}f(x)=\lim_{\substack{x_1 \rightarrow +\infty\\x_2 \rightarrow-\infty}}f(x)
=\lim_{\substack{x_1 \rightarrow -\infty\\x_2 \rightarrow+\infty}}f(x)
=\lim_{\substack{x_1 \rightarrow -\infty\\x_2 \rightarrow-\infty}}f(x)=+\infty$$
và $f(x)$ khả vi và liên tục $\forall (x_1, x_2) \in \mathbb{R}^2$. Vậy $x_1=x_2=1$ cũng là một cực tiểu toàn cục.