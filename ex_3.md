### 3 Cho $A \in \mathbb{R}^{m \times n}$ với $m > n$ và $\mathrm{rank}(A)=n$, $b \in \mathbb{R}^{m}$. Hãy giải bài toán tối ưu sau:

$$\min_x \lVert Ax - b \rVert_2^2$$

Cho $A \in \mathbb{R}^{m \times n}$ với $m > n$ và $\mathrm{rank}(A)=n, b \in \mathbb{R}^m$. Giải bài toán tối ưu:

$$\min_x \lVert Ax - b \rVert_2^2$$

Ta có $\mathrm{dom}\Big( \lVert Ax-b \rVert_2^2\Big)=\mathbb{R}^{n}$ là một tập lồi

Ta chứng minh
$\lVert Ax - b \rVert_2^2$ là hàm lồi:

$$\lVert Ax - b \rVert_2^2=(Ax-b)^T(Ax-b)=x^TA^TAx - x^TA^Tb - b^TAx + b^Tb (x^TA^Tb \text{ và } b^TAx \text{ là hai số vô hướng nên } (b^TAx)^T=x^TA^Tb=b^TAx)$$

$$\lVert Ax - b \rVert_2^2=x^TA^TAx - 2x^TA^Tb + b^Tb$$

$$\nabla \lVert Ax - b \rVert_2^2=(A^TA + (A^TA)^T)x-2A^Tb=2A^TAx - 2A^Tb$$

$$\nabla^2 \lVert Ax - b \rVert_2^2=2A^TA$$

Ta xét:

$$2p^TA^TAp=2(Ap)^TAp\geq0 \thickspace \forall p \in \mathbb{R}^{n} \Rightarrow 2A^TA \succeq 0$$

Ta có $\mathrm{dom}\Big( \lVert Ax-b \rVert_2^2\Big)=\mathbb{R}^{n}$ là một tập lồi và $\nabla^2 \lVert Ax - b \rVert_2^2 \succeq 0$. Vì Vậy $\lVert Ax - b \rVert_2^2$ là hàm lồi, điểm dừng của phương trình $\nabla \lVert Ax - b \rVert_2^2=0$ là cực tiểu toàn cục của bài toán.

Ta giải phương trình

$$\nabla \lVert Ax - b \rVert_2^2 = 2 A^T A x - 2 A^T b = 0$$

Với $\mathrm{rank}(A)=n$, ta chứng minh $A^T A$ khả nghịch.

Ta xét hệ phương trình:

$$A^T A x = 0 \Rightarrow x^T A^T A x = 0 \Leftrightarrow (Ax)^T (Ax) = 0 \Leftrightarrow \lVert Ax \rVert_2^2 =0 \Leftrightarrow Ax = 0$$

Do $\mathrm{rank}(A)=n$ nên các cột của $A$ độc lập tuyến tính vậy để $Ax=0 \Leftrightarrow x = 0$

Vậy $A^T A x = 0 \Leftrightarrow x = 0$, $A^T A$ khả nghịch.

$$\Rightarrow x = (A^TA)^{-1}A^T b$$

là cực tiểu toàn cục của bài toán