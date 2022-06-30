### 1 Hãy chứng minh các hàm sau là hàm lồi

#### 1.1 Ridge Regression:

$$f(x)=\lVert Ax - b \rVert_2^2 + \lambda \lVert x \rVert_2^2$$

$$f(x)=\lVert Ax - b \rVert_2^2 + \lambda \lVert x \rVert_2^2$$

Đặt $A \in \mathbb{R}^{m \times n}, b \in \mathbb{R}^{m}, x \in \mathbb{R}^{n}$, ta có $\mathrm{dom}(f)=\mathbb{R}^{n}$ là tập lồi

$$\Leftrightarrow f(x) = (Ax - b)^T (Ax - b) + \lambda x^T x$$

$$\Leftrightarrow f(x) = x^T A^T A x - x^TA^Tb - b^T Ax + b^T b + \lambda x^T x$$

Do $x^TA^Tb$ và $b^TAx$ là hai số vô hướng và $(x^TA^Tb)^T=b^TAx$ nên $x^TA^Tb=b^TAx$ (chuyển vị của một số vô hướng bằng chính nó) nên:

$$f(x) = x^T A^T A x - x^TA^Tb - b^T Ax + b^T b + \lambda x^T x=x^T A^T A x-2x^TA^Tb+b^Tb + \lambda x^T x$$

$$\nabla f(x) =(A^TA + (A^TA)^T)x - 2A^Tb + 2\lambda x = 2A^T A x - 2 A^T b + 2\lambda x$$

$$\nabla^2 f(x) = 2A^T A + 2 \lambda I$$

Ta xét:

$$p^T \nabla^2 f(x) p = 2 p^T A^T A p + 2\lambda p^Tp = 2 (Ap)^TAp + 2\lambda p^Tp \geq 0 \thickspace\forall \thickspace p \in \mathbb{R}^{n} $$

nên $$\nabla^2 f(x) \succeq 0$$

$\mathrm{dom}(f)$ là tập lồi và $\nabla^2 f(x) \succeq 0$ vì vậy hàm $f(x)$ là một hàm lồi


#### 1.2 Lasso Regression

$$f(x)=\lVert Ax - b \rVert_2^2 + \lambda \lVert x \rVert_1$$

Đặt $A \in \mathbb{R}^{m \times n}, b \in \mathbb{R}^{m}, x \in \mathbb{R}^{n}$, ta có $\mathrm{dom}(f)=\mathbb{R}^{n}$ là tập lồi.

$\mathrm{dom}(\lVert Ax - b \rVert_2^2)=\mathbb{R}^n$ và $\mathrm{dom}(\lVert x \rVert_1)=\mathbb{R}^n$

Ta chứng minh
$\lVert Ax - b \rVert_2^2$ là hàm lồi:

$$\lVert Ax - b \rVert_2^2=(Ax-b)^T(Ax-b)=x^TA^TAx - x^TA^Tb - b^TAx + b^Tb (x^TA^Tb \text{ và } b^TAx \text{ là hai số vô hướng nên } (b^TAx)^T=x^TA^Tb=b^TAx)$$

$$\lVert Ax - b \rVert_2^2=x^TA^TAx - 2x^TA^Tb + b^Tb$$

$$\nabla \lVert Ax - b \rVert_2^2=(A^TA + (A^TA)^T)x-2A^Tb=2A^TAx - 2A^Tb$$

$$\nabla^2 \lVert Ax - b \rVert_2^2=2A^TA$$

Ta xét:

$$2p^TA^TAp=2(Ap)^TAp\geq0 \thickspace \forall p \in \mathbb{R}^{n} \Rightarrow 2A^TA \succeq 0$$

và $\mathrm{dom}(\lVert Ax - b \rVert_2^2)=\mathbb{R}^n$ là tập lồi. Vậy $\lVert Ax - b \rVert_2^2$ là hàm lồi

Ta xét:

$$\lVert \theta x + (1-\theta)y \rVert_1 \leq \theta \lVert x \rVert_1 + (1-\theta)\lVert y \rVert_1 \thickspace \forall \thickspace \theta \in \lbrack 0, 1 \rbrack, x, y \in \mathbb{R}^n$$

theo bất đẳng thức tam giác và $\mathrm{dom}(\lVert x \rVert_1)=\mathbb{R}^n$ là tập lồi nên $\lVert x \rVert_1$ là hàm lồi. Tổng của hai hàm lồi là một hàm lồi nên $f(x)$ là một hàm lồi.

#### 1.3 Logistic Regression

$$f(w)=\dfrac{1}{n}\sum_{i=1}^n \Big( y_i x_i^T w + \ln(1 + e^{x_i^T w}) \Big)$$

với $(x_i, y_i) \in \mathbb{R}^{k+1},i=1,2,\dots,n$ là cặp dữ liệu đầu vào và nhãn tương ứng và $w \in \mathbb{R}^k$

Ta có $\mathrm{dom}(f)=\mathbb{R}^{k}$ là một tập lồi.

$$f(w)=\dfrac{1}{n}\sum_{i=1}^n \Big( y_i x_i^T w + \ln(1 + e^{x_i^T w}) \Big)$$

$$\Leftrightarrow \nabla f(w)=\dfrac{1}{n}\sum_{i=1}^n \Big( y_i x_i + \dfrac{e^{x_i^Tw}}{1 + e^{x_i^T w}}x_i \Big)$$

$$\Leftrightarrow \nabla^2 f(x) = \dfrac{1}{n}\sum_{i=1}^n \dfrac{e^{x_i^Tw}(1 + e^{x_i^T w})-e^{2x_i^T w}}{(1 + e^{x_i^T w})^2}x_i x_i^T=\dfrac{1}{n}\sum_{i=1}^n \dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}x_i x_i^T$$

Ta xét số hạng thứ $i$:

$$\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}x_i x_i^T$$

Ta xét:
$$\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}p^Tx_i x_i^T p=\Bigg(\sqrt{\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}} x_i^Tp\Bigg)^T\Bigg(\sqrt{\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}} x_i^Tp\Bigg)\geq 0 \thickspace \forall p \in \mathbb{R}^{k}$$


$$\Rightarrow p^T \nabla^2 f(x)p=\dfrac{1}{n}\sum_{i=1}^n \dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}p^Tx_i x_i^T=\dfrac{1}{n}\sum_{i=1}^n \Bigg(\sqrt{\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}} x_i^Tp\Bigg)^T\Bigg(\sqrt{\dfrac{e^{x_i^Tw}}{(1 + e^{x_i^T w})^2}} x_i^Tp\Bigg)\geq 0 \thickspace \forall p \in \mathbb{R}^{k}$$

Ta có $\mathrm{dom}(f)=\mathbb{R}^{k}$ là một tập lồi và $\nabla^2 f(x) \succeq 0$ nên $f(w)$ là hàm lồi