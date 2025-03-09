# 高等数学部分

## 一、极限与连续

### 1.1 函数极限

*   **定义**:
    *   $\epsilon - \delta$ 定义:  $\lim_{x \to x_0} f(x) = A \Leftrightarrow \forall \epsilon > 0, \exists \delta > 0$，当 $0 < |x - x_0| < \delta$ 时，有 $|f(x) - A| < \epsilon$。
    *   $\epsilon - N$ 定义: $\lim_{x \to \infty} f(x) = A \Leftrightarrow \forall \epsilon > 0, \exists N > 0$，当 $|x| > N$ 时，有 $|f(x) - A| < \epsilon$。

*   **性质**:
    *   唯一性: 若极限存在，则极限值唯一。
    *   局部有界性: 若 $\lim_{x \to x_0} f(x)$ 存在，则 $f(x)$ 在 $x_0$ 的某个去心邻域内有界。
    *   保号性:
        *   **脱帽法**: 若 $\lim_{x \to x_0} f(x) = A > 0$，则 $\exists \delta > 0$，当 $0 < |x - x_0| < \delta$ 时，有 $f(x) > 0$。
        *   **戴帽法**: 若 $\exists \delta > 0$，当 $0 < |x - x_0| < \delta$ 时，$f(x) \ge 0$，且 $\lim_{x \to x_0} f(x) = A$，则 $A \ge 0$。
    *   局部保序性: 若 $\lim_{x \to x_0} f(x) = A$, $\lim_{x \to x_0} g(x) = B$，且 $A < B$，则 $\exists \delta > 0$，当 $0 < |x - x_0| < \delta$ 时，有 $f(x) < g(x)$。
    *   极限的四则运算:  若 $\lim f(x)$ 和 $\lim g(x)$ 都存在，则：
        *   $\lim [f(x) \pm g(x)] = \lim f(x) \pm \lim g(x)$
        *   $\lim [f(x) \cdot g(x)] = \lim f(x) \cdot \lim g(x)$
        *   $\lim \frac{f(x)}{g(x)} = \frac{\lim f(x)}{\lim g(x)}$ (其中 $\lim g(x) \ne 0$)
    *   复合函数的极限: 若 $\lim_{x \to x_0} g(x) = u_0$, $\lim_{u \to u_0} f(u) = A$, 且 $\exists \delta_0 > 0$, 当$0<|x-x_0|<\delta _0$ 时,有$g(x) \ne u_0$,则 $\lim_{x \to x_0} f(g(x)) = A$.
    *   夹逼定理
    *   单调有界准则

*   **连续性**:
    *   定义:  $\lim_{x \to x_0} f(x) = f(x_0)$，则称 $f(x)$ 在 $x_0$ 处连续。
    *   间断点:
        *   第一类间断点:
            *   可去间断点:  左、右极限存在且相等，但不等于该点函数值或该点无定义。
            *   跳跃间断点:  左、右极限存在但不相等。
        *   第二类间断点:  左、右极限至少有一个不存在。
            *   无穷间断点
            *   振荡间断点

### 1.2 数列极限

*   **定义**: $\epsilon - N$ 定义:  $\lim_{n \to \infty} x_n = A \Leftrightarrow \forall \epsilon > 0, \exists N > 0$，当 $n > N$ 时，有 $|x_n - A| < \epsilon$。

*   **性质**:
    *   唯一性
    *   有界性
    *   保号性
    *   四则运算
    *   夹逼定理
    *   单调有界准则

*   **数列极限的求法**:
    *   **利用定义**
    *   **利用性质** (四则运算、夹逼定理、单调有界准则)
    *   **利用已知极限** (例如 $\lim_{n \to \infty} \sqrt[n]{n} = 1$, $\lim_{n \to \infty} \sqrt[n]{a} = 1$ (a > 0))
    *   **利用定积分定义**
    *   **利用级数收敛的必要条件**
    *    **递推型数列极限**
    *   **n项和，n项积的数列极限**

*   **海涅定理 (归结原则)**:  $\lim_{x \to x_0} f(x) = A \Leftrightarrow$ 对任何以 $x_0$ 为极限的数列 $\{x_n\}$ ($x_n \ne x_0$)，都有 $\lim_{n \to \infty} f(x_n) = A$。

### 1.3 重要极限与等价无穷小

*   **重要极限**:
    *   $\lim_{x \to 0} \frac{\sin x}{x} = 1$
    *   $\lim_{x \to 0} (1+x)^{\frac{1}{x}} = e$
    *   $\lim_{x \to \infty} (1+\frac{1}{x})^x = e$
*   **等价无穷小** (当 $x \to 0$ 时):
    *   $\sin x \sim x$
    *   $\tan x \sim x$
    *   $1 - \cos x \sim \frac{1}{2}x^2$
    *   $e^x - 1 \sim x$
    *   $\ln(1+x) \sim x$
    *   $(1+x)^\alpha - 1 \sim \alpha x$
    *   $arcsinx \sim x$
    *   $arctanx \sim x$
* **常用转化**:
    *   $a^x = e^{xlna}$
    *    $[f(x)]^{g(x)} = e^{g(x)ln[f(x)]}$
    *    $\lim_{x\to0}[f(x)]^{g(x)} = e^{\lim_{x\to0}g(x)ln[f(x)]}$, 其中 $f(x) \sim u(x)$, $g(x) \sim v(x)$

## 二、导数与微分

### 2.1 导数定义与性质

*   **导数定义**:
    *   $f'(x_0) = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} = \lim_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0}$
    *   左导数、右导数

*   **几何意义**:  曲线 $y = f(x)$ 在点 $(x_0, f(x_0))$ 处的切线斜率。

*   **可导与连续的关系**:
    *   可导必连续。
    *   连续不一定可导 (例如 $y = |x|$ 在 $x = 0$ 处)。

*   **导数应用**：
    * $f(x)$二阶连续可导，$f(0) = 0$,$f'(0) \gt 0$,任取曲线$y=f(x)$上一点$(x,f(x))$作切线,该切线在$x$轴的截距记为$u(x)$,则$\lim_{x \to 0}\frac{x}{u(x)}$

      解：切线方程为$Y-f(x)=f'(x)(X-x)$, 令$Y=0$, 得$u(x)=x-\frac{f(x)}{f'(x)}$, 由题意知$f(0)=0$,所以用洛必达法则
      $$\lim_{x \to 0} \frac{x}{u(x)} =\lim_{x \to 0} \frac{x}{x-\frac{f(x)}{f'(x)}}=\lim_{x \to 0} \frac{f'(x)x}{xf'(x)-f(x)} = \lim_{x \to 0}\frac{f'(x)+xf''(x)}{f'(x)+xf''(x)-f'(x)} = \lim_{x \to 0}\frac{f'(x)+xf''(x)}{xf''(x)} = \lim_{x \to 0}\frac{f'(x)}{xf''(x)} + 1$$
     又$f'(0) \ne 0$, 洛必达得
     $$\lim_{x \to 0}\frac{f'(x)}{xf''(x)} = \lim_{x \to 0} \frac{f''(x)}{f''(x) + xf'''(x)} = \lim_{x \to 0}\frac{1}{1+\frac{xf'''(x)}{f''(x)}} = 1$$
     因此，$\lim_{x \to 0}\frac{x}{u(x)} = 1+1 = \frac{1}{2}$
    * n阶导数存在，不一定能n阶可导. (用洛必达法则分析)

      反例：$f(x) = x^3\sin(\frac{1}{x}), x \ne 0; f(x)=0, x=0$.
      $f''(0)$存在，但$f''(x)$在$x=0$不连续.
    * n阶连续可导.（用泰勒展开分析）

      若$f(x)$在$x=0$处n阶连续可导，则由泰勒公式，$f(x)$可在$x=0$处展开成带有佩亚诺余项的泰勒公式:
      $$f(x) = f(0) + f'(0)x + \frac{f''(0)}{2!}x^2 + ... + \frac{f^{(n)}(0)}{n!}x^n + o(x^n)$$

* **高阶导数**

    * $(uv)^{(n)} = \sum_{k=0}^{n}C_{n}^{k}u^{(n-k)}v^{(k)}$ (莱布尼兹公式)
    * $(x+y+z)^{3} = x^{3} + y^{3} + z^{3} + 3xy^{2} + 3x^{2}y + 3xz^{2} + 3x^{2}z + 3yz^{2} + 3y^{2}z + 6xyz$
    * $(xyz)' = x'yz+xy'z+xyz'$

### 2.2 导数计算

*   **基本求导公式** (见上)

*   **复合函数求导** (链式法则):  若 $y = f(u)$, $u = g(x)$，则 $\frac{dy}{dx} = \frac{dy}{du} \cdot \frac{du}{dx} = f'(u) \cdot g'(x)$。

*   **隐函数求导**:
    *   方程 $F(x, y) = 0$ 确定隐函数 $y = y(x)$，求导时将 $y$ 看作 $x$ 的函数。
    *   对方程两边同时关于 $x$ 求导，解出 $\frac{dy}{dx}$。

*   **参数方程求导**:  若 $\begin{cases} x = x(t) \\ y = y(t) \end{cases}$，则 $\frac{dy}{dx} = \frac{dy/dt}{dx/dt} = \frac{y'(t)}{x'(t)}$。

*   **反函数求导**:  若 $y = f(x)$ 的反函数为 $x = f^{-1}(y)$，则 $\frac{dx}{dy} = \frac{1}{dy/dx} = \frac{1}{f'(x)}$。

### 2.3 微分中值定理与导数应用

*   **罗尔定理**:  若 $f(x)$ 满足：
    *   在 $[a, b]$ 上连续；
    *   在 $(a, b)$ 内可导；
    *   $f(a) = f(b)$；
    则 $\exists \xi \in (a, b)$，使得 $f'(\xi) = 0$。

*   **拉格朗日中值定理**:  若 $f(x)$ 满足：
    *   在 $[a, b]$ 上连续；
    *   在 $(a, b)$ 内可导；
    则 $\exists \xi \in (a, b)$，使得 $f'(\xi) = \frac{f(b) - f(a)}{b - a}$。

*   **柯西中值定理**:  若 $f(x)$ 和 $g(x)$ 满足：
    *   在 $[a, b]$ 上连续；
    *   在 $(a, b)$ 内可导；
    *   $g'(x) \ne 0$；
    则 $\exists \xi \in (a, b)$，使得 $\frac{f'(\xi)}{g'(\xi)} = \frac{f(b) - f(a)}{g(b) - g(a)}$。

*   **泰勒公式**:
    *   **带佩亚诺余项的泰勒公式**:
        $f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + ... + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + o((x - x_0)^n)$
    *   **带拉格朗日余项的泰勒公式**:
        $f(x) = f(x_0) + f'(x_0)(x - x_0) + \frac{f''(x_0)}{2!}(x - x_0)^2 + ... + \frac{f^{(n)}(x_0)}{n!}(x - x_0)^n + \frac{f^{(n+1)}(\xi)}{(n+1)!}(x - x_0)^{n+1}$ (其中 $\xi$ 介于 $x$ 与 $x_0$ 之间)

*   **函数单调性与极值**:
    *   **单调性**:
        *   $f'(x) > 0 \Rightarrow f(x)$ 单调递增
        *   $f'(x) < 0 \Rightarrow f(x)$ 单调递减
    *   **极值**:
        *   **必要条件**:  若 $f(x)$ 在 $x_0$ 处取得极值，且 $f'(x_0)$ 存在，则 $f'(x_0) = 0$ (驻点)。
        *   **第一充分条件**:  $f'(x)$ 在 $x_0$ 两侧异号。
        *   **第二充分条件**:  若 $f'(x_0) = 0$ 且 $f''(x_0) \ne 0$，则：
            *   $f''(x_0) > 0 \Rightarrow f(x_0)$ 为极小值
            *   $f''(x_0) < 0 \Rightarrow f(x_0)$ 为极大值
    *   **极值点、驻点、拐点**:
        * 极值点不一定是驻点. (例如 $y = |x|$ 在 $x=0$ 处)
        * 驻点可能是拐点.

*   **曲线凹凸性**:
    *   $f''(x) > 0 \Rightarrow f(x)$ 为凹函数 (下凸)
    *   $f''(x) < 0 \Rightarrow f(x)$ 为凸函数 (上凸)
    *   **拐点**:  凹凸性发生改变的点 (通常 $f''(x) = 0$ 或 $f''(x)$ 不存在)

*   **渐近线**:
    *   **水平渐近线**:  $\lim_{x \to \infty} f(x) = A$ 或 $\lim_{x \to -\infty} f(x) = A$
    *   **垂直渐近线**:  $\lim_{x \to x_0^+} f(x) = \infty$ 或 $\lim_{x \to x_0^-} f(x) = \infty$
    *   **斜渐近线**:  $\lim_{x \to \infty} \frac{f(x)}{x} = k$ 且 $\lim_{x \to \infty} [f(x) - kx] = b$ (其中 $k \ne 0$)

*   **曲率**:
    *   $K = \frac{|y''|}{(1 + y'^2)^{3/2}}$
    *   曲率圆、曲率半径

## 三、积分

### 3.1 不定积分

*   **定义**:  若 $F'(x) = f(x)$，则称 $F(x)$ 为 $f(x)$ 的一个原函数，记为 $\int f(x) dx = F(x) + C$。

*   **基本积分公式**:
    *   $\int x^a dx = \frac{x^{a+1}}{a+1} + C$ ($a \ne -1$)
    *   $\int \frac{1}{x} dx = \ln |x| + C$
    *   $\int \sin x dx = -\cos x + C$
    *   $\int \cos x dx = \sin x + C$
    *   $\int \sec^2 x dx = \tan x + C$
    *   $\int \csc^2 x dx = -\cot x + C$
    *   $\int \sec x \tan x dx = \sec x + C$
    *   $\int \csc x \cot x dx = -\csc x + C$
    *   $\int a^x dx = \frac{a^x}{\ln a} + C$
    *   $\int e^x dx = e^x + C$
    *   $\int \frac{1}{\sqrt{1-x^2}} dx = \arcsin x + C = -\arccos x + C$
    *   $\int \frac{1}{1+x^2} dx = \arctan x + C = -\text{arccot } x + C$
    *    $\int \frac{1}{\sqrt{a^{2} - x^{2}}}dx = arcsin\frac{x}{a} + C$
    *    $\int \frac{1}{a^{2} + x^{2}}dx = \frac{1}{a}arctan\frac{x}{a} + C$
    *    $\int \frac{1}{x^{2} - a^{2}}dx = \frac{1}{2a}ln|\frac{x-a}{x+a}| + C$
    *    $\int \frac{1}{\sqrt{x^{2} + a^{2}}}dx = ln|x + \sqrt{x^{2} + a^{2}}| + C$
    *    $\int \frac{1}{\sqrt{x^{2} - a^{2}}}dx = ln|x + \sqrt{x^{2} - a^{2}}| + C$
    *    $\int secxdx = ln|secx + tanx| + C$
    *    $\int cscxdx = ln|cscx - cotx| + C = -ln|cscx + cotx| + C$

*   **换元积分法**:
    *   **第一类换元法 (凑微分法)**:  $\int f(g(x)) g'(x) dx = \int f(u) du$ (其中 $u = g(x)$)
    *   **第二类换元法**:  $\int f(x) dx = \int f(x(t)) x'(t) dt$ (其中 $x = x(t)$)
        *   三角代换:
            *   $\sqrt{a^2 - x^2} \Rightarrow x = a \sin t$
            *   $\sqrt{a^2 + x^2} \Rightarrow x = a \tan t$
            *   $\sqrt{x^2 - a^2} \Rightarrow x = a \sec t$
        *   倒代换:  $x = \frac{1}{t}$
        *   幂代换:  $x = t^n$
        *   指数/对数代换:  $e^x = t$ 或 $\ln x = t$

*   **分部积分法**:  $\int u dv = uv - \int v du$
    *   反对幂指三 (优先选择作为 $u$ 的顺序)

*   **有理函数积分**:
    *   $\int \frac{P(x)}{Q(x)} dx$
    *   先化为真分式 (若为假分式)
    *   将分母分解为不可约因式的乘积
    *   将真分式拆分为部分分式之和
    *   分别对每个部分分式积分

### 3.2 定积分

*   **定积分定义**:
    $$\int_a^b f(x) dx = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i) \Delta x_i$$ 
    其中 $\lambda = \max\{\Delta x_1, \Delta x_2, ..., \Delta x_n\}$

*   **定积分性质**:
    *   线性性质: $\int_a^b [k_1 f(x) + k_2 g(x)] dx = k_1 \int_a^b f(x) dx + k_2 \int_a^b g(x) dx$
    *   区间可加性: $\int_a^b f(x) dx = \int_a^c f(x) dx + \int_c^b f(x) dx$
    *   保号性: 若在 $[a, b]$ 上 $f(x) \ge 0$，则 $\int_a^b f(x) dx \ge 0$
    *   估值定理: 若在 $[a, b]$ 上 $m \le f(x) \le M$，则 $m(b-a) \le \int_a^b f(x) dx \le M(b-a)$
    *   积分中值定理:
        *   **第一积分中值定理**: 若 $f(x)$ 在 $[a, b]$ 上连续，则 $\exists \xi \in [a, b]$，使得 $\int_a^b f(x) dx = f(\xi)(b-a)$
        *   **第二积分中值定理**: 若 $f(x)$ 在 $[a, b]$ 上连续，$g(x)$ 在 $[a, b]$ 上可积且不变号，则 $\exists \xi \in [a, b]$，使得 $\int_a^b f(x)g(x) dx = f(\xi) \int_a^b g(x) dx$

*   **变限积分**:
    *   $\Phi(x) = \int_a^x f(t) dt$
    *   $\Phi'(x) = f(x)$
    *   $\frac{d}{dx} \int_{a(x)}^{b(x)} f(t) dt = f(b(x))b'(x) - f(a(x))a'(x)$

*   **牛顿-莱布尼茨公式**:  若 $F(x)$ 是 $f(x)$ 在 $[a, b]$ 上的一个原函数，则 $\int_a^b f(x) dx = F(b) - F(a)$

*   **定积分的换元法与分部积分法** (与不定积分类似，但要注意积分限的变换)

*   **广义积分**:
    *   **无穷限积分**:
        *   $\int_a^{+\infty} f(x) dx = \lim_{b \to +\infty} \int_a^b f(x) dx$
        *   $\int_{-\infty}^b f(x) dx = \lim_{a \to -\infty} \int_a^b f(x) dx$
        *   $\int_{-\infty}^{+\infty} f(x) dx = \int_{-\infty}^c f(x) dx + \int_c^{+\infty} f(x) dx$
    *   **瑕积分** (无界函数的广义积分):
        *   若 $f(x)$ 在 $(a, b]$ 上连续，且 $\lim_{x \to a^+} f(x) = \infty$，则 $\int_a^b f(x) dx = \lim_{\epsilon \to 0^+} \int_{a+\epsilon}^b f(x) dx$
        *   类似定义瑕点在区间右端点或区间内部的情况

*   **几个定积分性质**
    *   $f(x)$不连续,则原函数存在与否 和 定积分存在与否 可以互不相干
    *   连续函数一定有原函数.
        证明：$\because f(x)$在$I$上连续, $\therefore [\int_{a}^{x}f(t)dt]' = f(x)$, $f(x)$是可导函数,可导必连续.
        故$f(x)$在$I$上必有原函数, 但不一定能表示成初等函数的形式.
    *   $f(x)$有第一类间断点和无穷间断点，可能存在原函数.
        例: $f(x) = 2xsin\frac{1}{x} - cos\frac{1}{x}, x \ne 0; f(0) = 0$, 原函数$F(x) = x^{2}sin\frac{1}{x} + C$
    *    有跳跃间断点，无原函数.
    *    积分的加减=加减的积分:$\int[f(x) \pm g(x)]dx = \int f(x)dx \pm \int g(x)dx$
    *    $\int_{0}^{a}f(x)dx = \int_{0}^{a}[f(x) + f(a-x)]dx$, 当$a=\pi$

### 3.3 定积分应用

*   **几何应用**:
    *   **平面图形面积**:
        *   直角坐标: $S = \int_a^b |f(x) - g(x)| dx$
        *   参数方程: $S = \int_\alpha^\beta |y(t)x'(t)| dt$
        *   极坐标: $S = \frac{1}{2} \int_\alpha^\beta r^2(\theta) d\theta$
    *   **旋转体体积**:
        *   **圆盘法**: $V = \pi \int_a^b [f(x)]^2 dx$ (绕 x 轴) 或 $V = \pi \int_c^d [g(y)]^2 dy$ (绕 y 轴)
        *   **壳法**: $V = 2\pi \int_a^b x|f(x)| dx$ (绕 y 轴) 或 $V = 2\pi \int_c^d y|g(y)| dy$ (绕 x 轴)
    *   **平面曲线弧长**:
        *   直角坐标: $s = \int_a^b \sqrt{1 + [f'(x)]^2} dx$
        *   参数方程: $s = \int_\alpha^\beta \sqrt{[x'(t)]^2 + [y'(t)]^2} dt$
        *   极坐标: $s = \int_\alpha^\beta \sqrt{r^2(\theta) + [r'(\theta)]^2} d\theta$
    *   **旋转曲面面积**:
        *   $S = 2\pi \int_a^b |f(x)|\sqrt{1 + [f'(x)]^2} dx$ (绕 x 轴)
    *   **平行截面面积已知的立体体积**:
        *   $V = \int_a^b A(x) dx$ (其中 $A(x)$ 为截面面积)

*   **物理应用**:
    *   **变力做功**: $W = \int_a^b F(x) dx$
    *   **水压力**: $P = \int_a^b \rho g h(x) w(x) dx$ (其中 $\rho$ 为密度，$g$ 为重力加速度，$h(x)$ 为深度，$w(x)$ 为宽度)
    *    **引力**: $F = G\frac{m_{1}m_{2}}{r^{2}}$, 对质量为$m$的质点，$F = G\int \frac{m\Delta m}{r^{2}}$
    *    **质心,形心**

## 四、多元函数微积分

### 4.1 多元函数基本概念

*   **多元函数的极限**:
    *   $\lim_{(x, y) \to (x_0, y_0)} f(x, y) = A$
    *   二元函数的极限存在，要求沿任何路径趋近的极限都存在且相等。

*   **多元函数的连续性**:
    *   $\lim_{(x, y) \to (x_0, y_0)} f(x, y) = f(x_0, y_0)$

*   **偏导数**:
    *   $f_x(x_0, y_0) = \frac{\partial f}{\partial x}(x_0, y_0) = \lim_{\Delta x \to 0} \frac{f(x_0 + \Delta x, y_0) - f(x_0, y_0)}{\Delta x}$
    *   $f_y(x_0, y_0) = \frac{\partial f}{\partial y}(x_0, y_0) = \lim_{\Delta y \to 0} \frac{f(x_0, y_0 + \Delta y) - f(x_0, y_0)}{\Delta y}$
    *   高阶偏导数 (若混合偏导数在区域内连续，则与求导次序无关)

*   **全微分**:
    *   $dz = \frac{\partial f}{\partial x} dx + \frac{\partial f}{\partial y} dy$
    *   可微的必要条件: 偏导数存在
    *   可微的充分条件: 偏导数连续

*   **可微性**:
    *   可微 $\Rightarrow$ 偏导数存在
    *   偏导数存在 $\nRightarrow$ 可微
    *   可微 $\Rightarrow$ 连续
    *   连续 $\nRightarrow$ 可微
    *   偏导数连续 $\Rightarrow$ 可微

### 4.2 多元函数微分法

*   **链式求导法则**:
    *   复合函数求导
    *   隐函数求导 (一个方程、方程组)
    *    全微分形式不变性
*   **偏导数计算**:
    *   显函数求偏导
    *   隐函数求偏导
    *   抽象函数求偏导

### 4.3 多元函数极值

*   **无条件极值**:
    *   **必要条件**: 若 $f(x, y)$ 在 $(x_0, y_0)$ 处取得极值，且偏导数存在，则 $f_x(x_0, y_0) = 0$, $f_y(x_0, y_0) = 0$ (驻点)。
    *   **充分条件**: 若 $f_x(x_0, y_0) = 0$, $f_y(x_0, y_0) = 0$，记 $A = f_{xx}(x_0, y_0)$, $B = f_{xy}(x_0, y_0)$, $C = f_{yy}(x_0, y_0)$，则：
        *   $AC - B^2 > 0$ 时，有极值：
            *   $A > 0 \Rightarrow$ 极小值
            *   $A < 0 \Rightarrow$ 极大值
        *   $AC - B^2 < 0$ 时，无极值
        *   $AC - B^2 = 0$ 时，无法判断

*   **条件极值** (拉格朗日乘数法):
    *   求 $f(x, y)$ 在约束条件 $\varphi(x, y) = 0$ 下的极值。
    *   构造拉格朗日函数: $L(x, y, \lambda) = f(x, y) + \lambda \varphi(x, y)$
    *   求偏导数: $\begin{cases} L_x = f_x + \lambda \varphi_x = 0 \\ L_y = f_y + \lambda \varphi_y = 0 \\ L_\lambda = \varphi(x, y) = 0 \end{cases}$
    *   解方程组，求出可能的极值点。

### 4.4 重积分

*   **二重积分**:
    *   **定义**: $\iint_D f(x, y) d\sigma = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i, \eta_i) \Delta \sigma_i$
    *   **几何意义**: 以 $D$ 为底，$z = f(x, y)$ 为顶的曲顶柱体体积。
    *   **性质**:
        *   线性性质
        *   区域可加性
        *   保号性
        *   估值定理
        *   积分中值定理
    *   **计算**:
        *   **直角坐标**:
            *   X 型区域: $\int_a^b dx \int_{y_1(x)}^{y_2(x)} f(x, y) dy$
            *   Y 型区域: $\int_c^d dy \int_{x_1(y)}^{x_2(y)} f(x, y) dx$
        *   **极坐标**: $\iint_D f(x, y) d\sigma = \iint_D f(r\cos\theta, r\sin\theta) r dr d\theta$
            *   $\int_\alpha^\beta d\theta \int_{r_1(\theta)}^{r_2(\theta)} f(r\cos\theta, r\sin\theta) r dr$
        *   **对称性**:
            *   关于 $x$ 轴、$y$ 轴、原点对称
            *   轮换对称性
        *   **变量代换**:
            *   $x = x(u, v)$, $y = y(u, v)$
            *   $\iint_D f(x, y) dx dy = \iint_{D'} f(x(u, v), y(u, v)) |J| du dv$ (其中 $J = \frac{\partial(x, y)}{\partial(u, v)}$ 为雅可比行列式)
        *    **积分次序交换**

*   **三重积分**:
    *   **定义**: $\iiint_\Omega f(x, y, z) dV = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i) \Delta V_i$
    *   **计算**:
        *   **直角坐标**: $\int_a^b dx \int_{y_1(x)}^{y_2(x)} dy \int_{z_1(x, y)}^{z_2(x, y)} f(x, y, z) dz$ (先单积分，再二重积分)
        *   **柱面坐标**: $\iiint_\Omega f(x, y, z) dV = \iiint_\Omega f(r\cos\theta, r\sin\theta, z) r dr d\theta dz$
        *   **球面坐标**: $\iiint_\Omega f(x, y, z) dV = \iiint_\Omega f(r\sin\varphi\cos\theta, r\sin\varphi\sin\theta, r\cos\varphi) r^2 \sin\varphi dr d\theta d\varphi$

*    **重积分应用**:
    *   **几何应用**:
        *   体积: $V = \iiint_\Omega dV$
        *   曲面面积: $S = \iint_D \sqrt{1 + (\frac{\partial z}{\partial x})^2 + (\frac{\partial z}{\partial y})^2} dx dy$
        *   质心: $\bar{x} = \frac{\iiint_\Omega x \rho(x, y, z) dV}{\iiint_\Omega \rho(x, y, z) dV}$, $\bar{y} = \frac{\iiint_\Omega y \rho(x, y, z) dV}{\iiint_\Omega \rho(x, y, z) dV}$, $\bar{z} = \frac{\iiint_\Omega z \rho(x, y, z) dV}{\iiint_\Omega \rho(x, y, z) dV}$ (其中 $\rho(x, y, z)$ 为密度)
    *    **物理应用**:
        *    质量: $M = \iiint_{\Omega}\rho(x,y,z)dV$
        *    转动惯量

*   **含参变量积分**

### 4.5 曲线积分与曲面积分

*   **第一型曲线积分**:
    *   **定义**: $\int_L f(x, y) ds = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i, \eta_i) \Delta s_i$
    *   **计算**:
        *   直角坐标: $\int_L f(x, y) ds = \int_a^b f(x, y(x)) \sqrt{1 + [y'(x)]^2} dx$
        *   参数方程: $\int_L f(x, y) ds = \int_\alpha^\beta f(x(t), y(t)) \sqrt{[x'(t)]^2 + [y'(t)]^2} dt$

*   **第二型曲线积分**:
    *   **定义**: $\int_L P(x, y) dx + Q(x, y) dy = \lim_{\lambda \to 0} \sum_{i=1}^n [P(\xi_i, \eta_i) \Delta x_i + Q(\xi_i, \eta_i) \Delta y_i]$
    *   **计算**:
        *   直角坐标: $\int_L P(x, y) dx + Q(x, y) dy = \int_a^b [P(x, y(x)) + Q(x, y(x))y'(x)] dx$
        *   参数方程: $\int_L P(x, y) dx + Q(x, y) dy = \int_\alpha^\beta [P(x(t), y(t))x'(t) + Q(x(t), y(t))y'(t)] dt$
    *   **格林公式**: 若 $P(x, y)$ 和 $Q(x, y)$ 在单连通区域 $D$ 上具有连续偏导数，则
        $$\oint_L P dx + Q dy = \iint_D (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) dx dy$$
        (其中 $L$ 为 $D$ 的正向边界曲线)
    *   **曲线积分与路径无关的条件**:
        *   $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
        *   存在函数 $u(x, y)$，使得 $du = P dx + Q dy$
        *   $\oint_C P dx + Q dy = 0$ (其中 $C$ 为任意闭曲线)

*   **第一型曲面积分**:
    *   **定义**: $\iint_\Sigma f(x, y, z) dS = \lim_{\lambda \to 0} \sum_{i=1}^n f(\xi_i, \eta_i, \zeta_i) \Delta S_i$
    *   **计算**: $\iint_\Sigma f(x, y, z) dS = \iint_D f(x, y, z(x, y)) \sqrt{1 + (\frac{\partial z}{\partial x})^2 + (\frac{\partial z}{\partial y})^2} dx dy$ (其中 $D$ 为 $\Sigma$ 在 $xOy$ 面上的投影区域)

*   **第二型曲面积分**:
    *   **定义**: $\iint_\Sigma P(x, y, z) dydz + Q(x, y, z) dzdx + R(x, y, z) dxdy = \lim_{\lambda \to 0} \sum_{i=1}^n [P(\xi_i, \eta_i, \zeta_i) \Delta y_i \Delta z_i + Q(\xi_i, \eta_i, \zeta_i) \Delta z_i \Delta x_i + R(\xi_i, \eta_i, \zeta_i) \Delta x_i \Delta y_i]$
    *   **计算**: $\iint_\Sigma P dydz + Q dzdx + R dxdy = \iint_D [\pm P(x, y, z(x, y)) \cdot \frac{\partial z}{\partial x} \pm Q(x, y, z(x, y)) \cdot \frac{\partial z}{\partial y} \pm R(x, y, z(x, y))] dx dy$ (其中 $D$ 为 $\Sigma$ 在 $xOy$ 面上的投影区域，正负号根据曲面侧的方向确定)
    *   **高斯公式**: 若 $P(x, y, z)$, $Q(x, y, z)$, $R(x, y, z)$ 在空间区域 $\Omega$ 上具有连续偏导数，则
        $$\iiint_\Omega (\frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z}) dV = \iint_\Sigma P dydz + Q dzdx + R dxdy$$ 
        (其中 $\Sigma$ 为 $\Omega$ 的外侧边界曲面)
    *   **斯托克斯公式**: 若 $P(x, y, z)$, $Q(x, y, z)$, $R(x, y, z)$ 在曲面 $\Sigma$ 上具有连续偏导数，则
        $$\oint_L P dx + Q dy + R dz = \iint_\Sigma (\frac{\partial R}{\partial y} - \frac{\partial Q}{\partial z}) dydz + (\frac{\partial P}{\partial z} - \frac{\partial R}{\partial x}) dzdx + (\frac{\partial Q}{\partial x} - \frac{\partial P}{\partial y}) dxdy$$ 
        (其中 $L$ 为 $\Sigma$ 的边界曲线，方向与曲面侧符合右手定则)

## 五、常微分方程

### 5.1 一阶微分方程

*   **可分离变量方程**:
    *   $\frac{dy}{dx} = f(x)g(y)$
    *   分离变量: $\frac{dy}{g(y)} = f(x) dx$
    *   两边积分: $\int \frac{dy}{g(y)} = \int f(x) dx$

*   **齐次方程**:
    *   $\frac{dy}{dx} = f(\frac{y}{x})$
    *   令 $u = \frac{y}{x}$，则 $y = ux$, $\frac{dy}{dx} = u + x\frac{du}{dx}$
    *   代入原方程，化为可分离变量方程

*   **一阶线性方程**:
    *   $\frac{dy}{dx} + P(x)y = Q(x)$
    *   **常数变易法**:
        *   先解对应的齐次方程: $\frac{dy}{dx} + P(x)y = 0$，得到通解 $y = Ce^{-\int P(x) dx}$
        *   将常数 $C$ 换成函数 $C(x)$，代入原方程，求出 $C(x)$
        *   得到原方程的通解: $y = C(x)e^{-\int P(x) dx}$
    *   **公式法**: $y = e^{-\int P(x) dx} [\int Q(x) e^{\int P(x) dx} dx + C]$

*   **伯努利方程**:
    *   $\frac{dy}{dx} + P(x)y = Q(x)y^n$ ($n \ne 0, 1$)
    *   令 $z = y^{1-n}$，则 $\frac{dz}{dx} = (1-n)y^{-n}\frac{dy}{dx}$
    *   代入原方程，化为一阶线性方程

*    **全微分方程**:
*    $P(x,y)dx + Q(x,y)dy = 0$
    *   $\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
    *   $u = \int_{x_{0}}^{x}P(x,y_{0})dx + \int_{y_{0}}^{y}Q(x,y)dy$

### 5.2 高阶微分方程

*   **可降阶方程**:
    *   $y'' = f(x)$ 型:  连续两次积分即可。
    *   $y'' = f(x, y')$ 型:  令 $p = y'$，则 $y'' = p' = \frac{dp}{dx}$，化为一阶方程。
    *   $y'' = f(y, y')$ 型:  令 $p = y'$，则 $y'' = p' = \frac{dp}{dx} = \frac{dp}{dy} \cdot \frac{dy}{dx} = p \frac{dp}{dy}$，化为一阶方程。

*   **线性微分方程解的结构**:
    *   **齐次线性方程**: $y'' + p(x)y' + q(x)y = 0$
        *   若 $y_1(x)$ 和 $y_2(x)$ 是方程的两个线性无关的解，则 $y = C_1 y_1(x) + C_2 y_2(x)$ 为方程的通解。
    *   **非齐次线性方程**: $y'' + p(x)y' + q(x)y = f(x)$
        *   若 $y^*(x)$ 是方程的一个特解，$Y(x)$ 是对应齐次方程的通解，则 $y = Y(x) + y^*(x)$ 为方程的通解。
        *   若 $y_1^*(x)$ 和 $y_2^*(x)$ 分别是方程 $y'' + p(x)y' + q(x)y = f_1(x)$ 和 $y'' + p(x)y' + q(x)y = f_2(x)$ 的特解，则 $y_1^*(x) + y_2^*(x)$ 是方程 $y'' + p(x)y' + q(x)y = f_1(x) + f_2(x)$ 的特解。

*   **常系数线性微分方程**:
    *   **齐次方程**: $y'' + py' + qy = 0$
        *   特征方程: $r^2 + pr + q = 0$
        *   根据特征根的不同情况，通解的形式如下：
            *   两个不相等的实根 $r_1$, $r_2$:  $y = C_1 e^{r_1 x} + C_2 e^{r_2 x}$
            *   两个相等的实根 $r$:  $y = (C_1 + C_2 x)e^{rx}$
            *   一对共轭复根 $r = \alpha \pm i\beta$:  $y = e^{\alpha x} (C_1 \cos \beta x + C_2 \sin \beta x)$
    *   **非齐次方程**: $y'' + py' + qy = f(x)$
        *   **待定系数法**: 根据 $f(x)$ 的形式，设出特解的形式，代入原方程，确定待定系数。
            *   $f(x) = P_n(x)e^{kx}$:  $y^* = x^m Q_n(x) e^{kx}$ (其中 $m$ 为特征方程中根 $k$ 的重数)
            *   $f(x) = e^{kx}[P_l(x) \cos \omega x + P_n(x) \sin \omega x]$:  $y^* = x^m e^{kx} [Q_m(x) \cos \omega x + R_m(x) \sin \omega x]$ (其中 $m$ 为特征方程中根 $k \pm i\omega$ 的重数，$m = \max\{l, n\}$)
        *   **常数变易法**:
            *   先求出对应齐次方程的通解: $y = C_1 y_1(x) + C_2 y_2(x)$
            *   将常数 $C_1$ 和 $C_2$ 换成函数 $C_1(x)$ 和 $C_2(x)$，代入原方程，得到关于 $C_1'(x)$ 和 $C_2'(x)$ 的方程组
            *   解出 $C_1'(x)$ 和 $C_2'(x)$，积分得到 $C_1(x)$ 和 $C_2(x)$
            *   得到原方程的特解: $y^* = C_1(x) y_1(x) + C_2(x) y_2(x)$

*   **欧拉方程**:
    *   $x^2 y'' + pxy' + qy = f(x)$
    *   令 $x = e^t$ 或 $t = \ln x$，则 $\frac{dy}{dx} = \frac{1}{x}\frac{dy}{dt}$, $\frac{d^2y}{dx^2} = \frac{1}{x^2}(\frac{d^2y}{dt^2} - \frac{dy}{dt})$
    *   代入原方程，化为常系数线性微分方程

## 六、无穷级数

### 6.1 数项级数

*   **级数收敛的定义**:  若级数 $\sum_{n=1}^\infty u_n$ 的部分和数列 $\{S_n\}$ 收敛，则称级数收敛，其和为 $S = \lim_{n \to \infty} S_n$。

*   **级数收敛的柯西准则**:  级数 $\sum_{n=1}^\infty u_n$ 收敛的充要条件是：$\forall \epsilon > 0, \exists N > 0$，当 $n > N$ 时，对 $\forall p \in N$，有 $|u_{n+1} + u_{n+2} + ... + u_{n+p}| < \epsilon$。

*   **级数收敛的必要条件**:  若级数 $\sum_{n=1}^\infty u_n$ 收敛，则 $\lim_{n \to \infty} u_n = 0$。

*   **正项级数**:
    *   **比较判别法**:
        *   **一般形式**: 若 $u_n \le v_n$，且 $\sum_{n=1}^\infty v_n$ 收敛，则 $\sum_{n=1}^\infty u_n$ 收敛；若 $u_n \ge v_n$，且 $\sum_{n=1}^\infty v_n$ 发散，则 $\sum_{n=1}^\infty u_n$ 发散。
        *   **极限形式**: 若 $\lim_{n \to \infty} \frac{u_n}{v_n} = l$ ($0 \le l \le +\infty$)，则：
            *   $0 < l < +\infty$ 时，两级数同敛散
            *   $l = 0$ 时，若 $\sum_{n=1}^\infty v_n$ 收敛，则 $\sum_{n=1}^\infty u_n$ 收敛
            *   $l = +\infty$ 时，若 $\sum_{n=1}^\infty v_n$ 发散，则 $\sum_{n=1}^\infty u_n$ 发散
    *   **比值判别法 (达朗贝尔判别法)**: 若 $\lim_{n \to \infty} \frac{u_{n+1}}{u_n} = \rho$，则：
        *   $\rho < 1$ 时，级数收敛
        *   $\rho > 1$ 时，级数发散
        *   $\rho = 1$ 时，判别法失效
    *   **根值判别法 (柯西判别法)**: 若 $\lim_{n \to \infty} \sqrt[n]{u_n} = \rho$，则：
        *   $\rho < 1$ 时，级数收敛
        *   $\rho > 1$ 时，级数发散
        *   $\rho = 1$ 时，判别法失效
    *   **积分判别法**: 若 $f(x)$ 在 $[1, +\infty)$ 上单调递减且非负，则级数 $\sum_{n=1}^\infty f(n)$ 与广义积分 $\int_1^{+\infty} f(x) dx$ 同敛散。

*   **交错级数**:
    *   **莱布尼茨判别法**: 若交错级数 $\sum_{n=1}^\infty (-1)^{n-1} u_n$ ($u_n > 0$) 满足：
        *   $u_{n+1} \le u_n$ (单调递减)
        *   $\lim_{n \to \infty} u_n = 0$
        则级数收敛。

*   **绝对收敛与条件收敛**:
    *   若 $\sum_{n=1}^\infty |u_n|$ 收敛，则称 $\sum_{n=1}^\infty u_n$ 绝对收敛。
    *   若 $\sum_{n=1}^\infty u_n$ 收敛，但 $\sum_{n=1}^\infty |u_n|$ 发散，则称 $\sum_{n=1}^\infty u_n$ 条件收敛。
    *   绝对收敛的级数一定收敛。

### 6.2 幂级数

*   **定义**:  形如 $\sum_{n=0}^\infty a_n (x - x_0)^n$ 的级数称为幂级数。

*   **阿贝尔定理**:  对于幂级数 $\sum_{n=0}^\infty a_n x^n$，
    *   若它在 $x = x_1$ ($x_1 \ne 0$) 处收敛，则当 $|x| < |x_1|$ 时，它绝对收敛；
    *    若它在$x = x_1$处发散, 则当$|x| \gt |x_1|$时, 它发散。
*   **收敛半径与收敛区间**:
    *   **收敛半径**: $R = \lim_{n \to \infty} |\frac{a_n}{a_{n+1}}|$ 或 $R = \frac{1}{\lim_{n \to \infty} \sqrt[n]{|a_n|}}$ (若极限存在)
    *   **收敛区间**: $(-R, R)$ (端点处的敛散性需单独讨论)
    *   **收敛域**: 收敛区间及收敛的端点

*   **幂级数运算**:
    *   **加减法**: $\sum_{n=0}^\infty a_n x^n \pm \sum_{n=0}^\infty b_n x^n = \sum_{n=0}^\infty (a_n \pm b_n) x^n$ (收敛区间为两者交集)
    *   **乘法** (柯西乘积): $(\sum_{n=0}^\infty a_n x^n)(\sum_{n=0}^\infty b_n x^n) = \sum_{n=0}^\infty c_n x^n$ (其中 $c_n = \sum_{k=0}^n a_k b_{n-k}$) (收敛区间为两者交集)
    *   **求导与积分**:  幂级数在收敛区间内可逐项求导与逐项积分，且求导或积分后收敛半径不变。

*   **泰勒级数与麦克劳林级数**:
    *   **泰勒级数**: 若 $f(x)$ 在 $x_0$ 的某个邻域内具有任意阶导数，则
        $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(x_0)}{n!} (x - x_0)^n$$
    *   **麦克劳林级数**: $x_0 = 0$ 时的泰勒级数
        $$f(x) = \sum_{n=0}^\infty \frac{f^{(n)}(0)}{n!} x^n$$

*   **函数的幂级数展开**:
    *   **直接展开法** (利用泰勒公式)
    *   **间接展开法** (利用已知函数的幂级数展开式，通过变量代换、逐项求导、逐项积分等方法)
    *   **常用函数的麦克劳林级数**:
        *   $e^x = \sum_{n=0}^\infty \frac{x^n}{n!}$ ($-\infty < x < +\infty$)
        *   $\sin x = \sum_{n=0}^\infty (-1)^n \frac{x^{2n+1}}{(2n+1)!}$ ($-\infty < x < +\infty$)
        *   $\cos x = \sum_{n=0}^\infty (-1)^n \frac{x^{2n}}{(2n)!}$ ($-\infty < x < +\infty$)
        *   $\ln(1+x) = \sum_{n=1}^\infty (-1)^{n-1} \frac{x^n}{n}$ ($-1 < x \le 1$)
        *   $\frac{1}{1-x} = \sum_{n=0}^\infty x^n$ ($-1 < x < 1$)
        *   $(1+x)^\alpha = 1 + \sum_{n=1}^\infty \frac{\alpha(\alpha-1)...(\alpha-n+1)}{n!} x^n$ ($-1 < x < 1$)

### 6.3 傅里叶级数

*   **三角函数系的正交性**:
    *   $\{1, \cos x, \sin x, \cos 2x, \sin 2x, ..., \cos nx, \sin nx, ...\}$ 在 $[-\pi, \pi]$ 上正交，即任意两个不同的函数乘积在 $[-\pi, \pi]$ 上的积分为 0。

*   **傅里叶级数**:
    *   若 $f(x)$ 在 $[-\pi, \pi]$ 上可积，则
        $$f(x) \sim \frac{a_0}{2} + \sum_{n=1}^\infty (a_n \cos nx + b_n \sin nx)$$
        其中
        $$a_n = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \cos nx dx$$
        $$b_n = \frac{1}{\pi} \int_{-\pi}^\pi f(x) \sin nx dx$$
        称为 $f(x)$ 的傅里叶系数。

*   **正弦级数与余弦级数**:
    *   **正弦级数**: 若 $f(x)$ 为 $[-\pi, \pi]$ 上的奇函数，则 $a_n = 0$,
        $$f(x) \sim \sum_{n=1}^\infty b_n \sin nx$$
        其中 $b_n = \frac{2}{\pi} \int_0^\pi f(x) \sin nx dx$
    *   **余弦级数**: 若 $f(x)$ 为 $[-\pi, \pi]$ 上的偶函数，则 $b_n = 0$,
        $$f(x) \sim \frac{a_0}{2} + \sum_{n=1}^\infty a_n \cos nx$$
        其中 $a_n = \frac{2}{\pi} \int_0^\pi f(x) \cos nx dx$

*   **狄利克雷收敛定理**:  若 $f(x)$ 在 $[-\pi, \pi]$ 上满足：
    *   连续或只有有限个第一类间断点；
    *   只有有限个极值点；
    则 $f(x)$ 的傅里叶级数收敛，且：
        *   当 $x$ 为 $f(x)$ 的连续点时，级数收敛于 $f(x)$；
        *   当 $x$ 为 $f(x)$ 的间断点时，级数收敛于 $\frac{f(x^-) + f(x^+)}{2}$。
对不起，之前的确在第七节之后的内容有所简略，没有完全展开。您批评得对，我这就开始补充第七节及其之后内容的详细版本，并尽可能配上图形说明（由于Markdown本身不支持直接绘图，我会用文字描述图形，或者用ASCII art来示意）：

## 七、向量代数与空间解析几何

### 7.1 向量代数

*   **向量**: 既有大小又有方向的量。记作 $\vec{a}$ 或 **a** (粗体)。
    *   **向量的模**: 向量的大小 (长度)，记作 $|\vec{a}|$。
    *   **单位向量**: 模为 1 的向量。
    *   **零向量**: 模为 0 的向量，记作 $\vec{0}$ 或 **0**。零向量的方向是任意的。
    *   **向量的加法/减法**: 平行四边形法则 或 三角形法则。
        *   (图形描述：平行四边形法则 - 两个向量共起点，以这两个向量为邻边作平行四边形，对角线为和向量；三角形法则 - 两个向量首尾相接，从第一个向量的起点指向第二个向量的终点的向量为和向量)
        *   运算律:
            *   交换律: $\vec{a} + \vec{b} = \vec{b} + \vec{a}$
            *   结合律: $(\vec{a} + \vec{b}) + \vec{c} = \vec{a} + (\vec{b} + \vec{c})$
    *   **数乘向量**: $k\vec{a}$
        *   $k > 0$: 与 $\vec{a}$ 同向，$|k\vec{a}| = k|\vec{a}|$
        *   $k < 0$: 与 $\vec{a}$ 反向，$|k\vec{a}| = |k||\vec{a}|$
        *   $k = 0$: $k\vec{a} = \vec{0}$
        *   运算律:
            *   $k(l\vec{a}) = (kl)\vec{a}$
            *   $(k+l)\vec{a} = k\vec{a} + l\vec{a}$
            *   $k(\vec{a} + \vec{b}) = k\vec{a} + k\vec{b}$

*   **线性组合，线性表示，线性相关，线性无关**:
    *   **线性组合**:  $k_1 \vec{a_1} + k_2 \vec{a_2} + ... + k_n \vec{a_n}$
    *   **线性表示**:  向量 $\vec{b}$ 可以表示为向量组 $\vec{a_1}, \vec{a_2}, ..., \vec{a_n}$ 的线性组合。
    *   **线性相关**: 存在不全为零的 $k_1, k_2, ..., k_n$，使得 $k_1 \vec{a_1} + k_2 \vec{a_2} + ... + k_n \vec{a_n} = \vec{0}$。
        *    几何意义(二维): 向量共线
        *    几何意义(三维): 向量共面
    *   **线性无关**: 只有当 $k_1 = k_2 = ... = k_n = 0$ 时，才能使 $k_1 \vec{a_1} + k_2 \vec{a_2} + ... + k_n \vec{a_n} = \vec{0}$。
*   **数量积 (点积)**:
    *   $\vec{a} \cdot \vec{b} = |\vec{a}| |\vec{b}| \cos \theta$ (其中 $\theta$ 为 $\vec{a}$ 与 $\vec{b}$ 的夹角, $0 \le \theta \le \pi$)
    *   (图形描述：$\vec{a}$ 在 $\vec{b}$ 上的投影乘以 $\vec{b}$ 的模长)
    *   性质:
        *   $\vec{a} \cdot \vec{a} = |\vec{a}|^2$
        *   $\vec{a} \cdot \vec{b} = \vec{b} \cdot \vec{a}$ (交换律)
        *   $(k\vec{a}) \cdot \vec{b} = k(\vec{a} \cdot \vec{b}) = \vec{a} \cdot (k\vec{b})$
        *   $(\vec{a} + \vec{b}) \cdot \vec{c} = \vec{a} \cdot \vec{c} + \vec{b} \cdot \vec{c}$ (分配律)
        *   $\vec{a} \perp \vec{b} \Leftrightarrow \vec{a} \cdot \vec{b} = 0$
    *    坐标表示：若 $\vec{a} = (a_1, a_2, a_3)$, $\vec{b} = (b_1, b_2, b_3)$，则 $\vec{a} \cdot \vec{b} = a_1 b_1 + a_2 b_2 + a_3 b_3$
*   **向量积 (叉积)**:
    *   $\vec{a} \times \vec{b} = \vec{c}$
        *   $|\vec{c}| = |\vec{a}| |\vec{b}| \sin \theta$ (其中 $\theta$ 为 $\vec{a}$ 与 $\vec{b}$ 的夹角, $0 \le \theta \le \pi$)
        *   $\vec{c}$ 的方向垂直于 $\vec{a}$ 与 $\vec{b}$ 所在的平面，且 $\vec{a}$, $\vec{b}$, $\vec{c}$ 符合右手定则。
        *   (图形描述：右手四指从 $\vec{a}$ 转向 $\vec{b}$，拇指指向为 $\vec{c}$ 的方向)
    *   几何意义: $|\vec{a} \times \vec{b}|$ 等于以 $\vec{a}$ 和 $\vec{b}$ 为邻边的平行四边形的面积。
    *   性质:
        *   $\vec{a} \times \vec{a} = \vec{0}$
        *   $\vec{a} \times \vec{b} = -(\vec{b} \times \vec{a})$ (反交换律)
        *   $(k\vec{a}) \times \vec{b} = k(\vec{a} \times \vec{b}) = \vec{a} \times (k\vec{b})$
        *   $(\vec{a} + \vec{b}) \times \vec{c} = \vec{a} \times \vec{c} + \vec{b} \times \vec{c}$ (分配律)
        *   $\vec{a} \parallel \vec{b} \Leftrightarrow \vec{a} \times \vec{b} = \vec{0}$
     * 坐标表示: 若$\vec a = (a_1, a_2, a_3)$, $\vec b = (b_1, b_2,b_3)$, 则
        $$\vec a \times \vec b = \begin{vmatrix} \vec i & \vec j & \vec k \\ a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \end{vmatrix} = (a_2b_3 - a_3b_2)\vec i + (a_3b_1 - a_1b_3)\vec j + (a_1b_2 - a_2b_1)\vec k$$
*   **混合积**:
    *   $(\vec{a} \times \vec{b}) \cdot \vec{c}$ (记作 $[\vec{a} \vec{b} \vec{c}]$)
    *   几何意义: 以 $\vec{a}$, $\vec{b}$, $\vec{c}$ 为棱的平行六面体的体积 (带正负号)。
    *   性质:
        *   $[\vec{a} \vec{b} \vec{c}] = [\vec{b} \vec{c} \vec{a}] = [\vec{c} \vec{a} \vec{b}] = -[\vec{a} \vec{c} \vec{b}] = -[\vec{b} \vec{a} \vec{c}] = -[\vec{c} \vec{b} \vec{a}]$
        *   $\vec{a}, \vec{b}, \vec{c}$ 共面 $\Leftrightarrow [\vec{a} \vec{b} \vec{c}] = 0$
     *    坐标表示: $[\vec{a} \vec{b} \vec{c}] = \begin{vmatrix} a_1 & a_2 & a_3 \\ b_1 & b_2 & b_3 \\ c_1 & c_2 & c_3 \end{vmatrix}$

*   **向量的夹角、投影**:
    *   夹角: $\cos \theta = \frac{\vec{a} \cdot \vec{b}}{|\vec{a}| |\vec{b}|}$
    *   投影: $(\vec{a})_{\vec{b}} = \frac{\vec{a} \cdot \vec{b}}{|\vec{b}|} = |\vec{a}|\cos\theta$ (向量 $\vec{a}$ 在向量 $\vec{b}$ 上的投影，是一个数量)

### 7.2 平面与直线

*   **平面方程**:
    *   **点法式**: $A(x - x_0) + B(y - y_0) + C(z - z_0) = 0$
        *   $(x_0, y_0, z_0)$ 为平面上一点，$\vec{n} = (A, B, C)$ 为平面的法向量。
        *   (图形描述：法向量垂直于平面)
    *   **一般式**: $Ax + By + Cz + D = 0$
        *   $(A, B, C)$ 为平面的法向量。
    *   **截距式**: $\frac{x}{a} + \frac{y}{b} + \frac{z}{c} = 1$
        *   $a$, $b$, $c$ 分别为平面在 $x$, $y$, $z$ 轴上的截距 (不为0)。
    *   **三点式**: $\begin{vmatrix} x - x_1 & y - y_1 & z - z_1 \\ x_2 - x_1 & y_2 - y_1 & z_2 - z_1 \\ x_3 - x_1 & y_3 - y_1 & z_3 - z_1 \end{vmatrix} = 0$
        *   $(x_1, y_1, z_1)$, $(x_2, y_2, z_2)$, $(x_3, y_3, z_3)$ 为平面上不共线的三点。

*   **直线方程**:
    *   **点向式 (对称式)**: $\frac{x - x_0}{m} = \frac{y - y_0}{n} = \frac{z - z_0}{p}$
        *   $(x_0, y_0, z_0)$ 为直线上一点，$\vec{s} = (m, n, p)$ 为直线的方向向量。
        *   (图形描述: 方向向量平行于直线)
    *   **参数式**: $\begin{cases} x = x_0 + mt \\ y = y_0 + nt \\ z = z_0 + pt \end{cases}$  ($t$ 为参数)
    *   **一般式**: $\begin{cases} A_1x + B_1y + C_1z + D_1 = 0 \\ A_2x + B_2y + C_2z + D_2 = 0 \end{cases}$ (两个平面的交线)
        *   直线的方向向量: $\vec{s} = \vec{n_1} \times \vec{n_2}$ (其中 $\vec{n_1} = (A_1, B_1, C_1)$, $\vec{n_2} = (A_2, B_2, C_2)$ 为两个平面的法向量)
    * **两点式**:$\frac{x-x_{1}}{x_{2} - x_{1}} = \frac{y - y_{1}}{y_{2}-y_{1}} = \frac{z-z_{1}}{z_{2}-z_{1}}$
*   **位置关系**:
    *   **平面与平面**:
        *   平行: $\frac{A_1}{A_2} = \frac{B_1}{B_2} = \frac{C_1}{C_2} \ne \frac{D_1}{D_2}$ 或 $\vec{n_1} \parallel \vec{n_2}$ 且 $D_1 \ne D_2$
        *   垂直: $A_1 A_2 + B_1 B_2 + C_1 C_2 = 0$ 或 $\vec{n_1} \cdot \vec{n_2} = 0$
        *   重合: $\frac{A_1}{A_2} = \frac{B_1}{B_2} = \frac{C_1}{C_2} = \frac{D_1}{D_2}$
        *   夹角: $\cos \theta = \frac{|A_1 A_2 + B_1 B_2 + C_1 C_2|}{\sqrt{A_1^2 + B_1^2 + C_1^2} \sqrt{A_2^2 + B_2^2 + C_2^2}} = \frac{|\vec{n_1} \cdot \vec{n_2}|}{|\vec{n_1}| |\vec{n_2}|}$
    *   **直线与直线**:
        *   平行: $\frac{m_1}{m_2} = \frac{n_1}{n_2} = \frac{p_1}{p_2}$ 或 $\vec{s_1} \parallel \vec{s_2}$
        *   垂直: $m_1 m_2 + n_1 n_2 + p_1 p_2 = 0$ 或 $\vec{s_1} \cdot \vec{s_2} = 0$
        *   共面: $[\vec{s_1} \vec{s_2} \vec{P_1 P_2}] = 0$
        *   异面: $[\vec{s_1} \vec{s_2} \vec{P_1 P_2}] \ne 0$
        *   夹角: $\cos \theta = \frac{|m_1 m_2 + n_1 n_2 + p_1 p_2|}{\sqrt{m_1^2 + n_1^2 + p_1^2} \sqrt{m_2^2 + n_2^2 + p_2^2}} = \frac{|\vec{s_1} \cdot \vec{s_2}|}{|\vec{s_1}| |\vec{s_2}|}$
        *    公垂线: 同时垂直于两条异面直线的直线
    *   **直线与平面**:
        *   平行: $Am + Bn + Cp = 0$ 或 $\vec{n} \cdot \vec{s} = 0$
        *   垂直: $\frac{A}{m} = \frac{B}{n} = \frac{C}{p}$ 或 $\vec{n} \parallel \vec{s}$
        *   直线在平面上: $\begin{cases} Am + Bn + Cp = 0 \\ Ax_0 + By_0 + Cz_0 + D = 0 \end{cases}$ (直线的方向向量与平面法向量垂直，且直线上一点在平面上)
        *   夹角: $\sin \theta = \frac{|Am + Bn + Cp|}{\sqrt{A^2 + B^2 + C^2} \sqrt{m^2 + n^2 + p^2}} = \frac{|\vec{n} \cdot \vec{s}|}{|\vec{n}| |\vec{s}|}$

*   **距离**:
    *   **点到平面**: $d = \frac{|Ax_0 + By_0 + Cz_0 + D|}{\sqrt{A^2 + B^2 + C^2}}$
    *   **点到直线**: $d = \frac{|\vec{s} \times \vec{P_0 P}|}{|\vec{s}|}$ (其中 $\vec{s}$ 为直线方向向量，$P_0(x_0,y_0,z_0)$ 为直线上一点，$P(x,y,z)$ 为直线外一点)
    *   **两平行平面之间的距离**: $d = \frac{|D_1 - D_2|}{\sqrt{A^2 + B^2 + C^2}}$
    *   **两直线间**:
        *   平行直线之间的距离: 在其中一条直线上取一点, 按照点到直线的距离计算.
        *   异面直线之间的距离: $d = \frac{|[\vec{s_1} \vec{s_2} \vec{P_1 P_2}]|}{|\vec{s_1} \times \vec{s_2}|}$ (其中 $\vec{s_1}$, $\vec{s_2}$ 为两直线方向向量，$P_1$, $P_2$ 分别为两直线上一点)
        *   公垂线: 同时垂直于两条异面直线的直线, 距离为公垂线段的长度.

### 7.3 曲面与曲线

*   **旋转曲面**:
    *   定义: 一条平面曲线 $C$ 绕同一平面上的定直线 $l$ (旋转轴) 旋转一周所形成的曲面。曲线 $C$ 叫做母线，$l$ 叫做旋转轴。
    *   $yOz$ 面上的曲线$f(y,z) = 0$绕$z$轴旋转开形成的旋转曲面: $f(\pm\sqrt{x^{2}+y^{2}}, z) = 0$
    *   $yOz$ 面上的曲线$f(y,z) = 0$绕$y$轴旋转开形成的旋转曲面: $f(y, \pm\sqrt{x^{2}+z^{2}}) = 0$

*   **柱面**:
    *   定义: 动直线 $l$ (母线) 沿给定曲线 $C$ (准线) 平行移动所形成的曲面。
    *    方程中缺少的变量对应的坐标轴为母线。 例如$f(x,y) = 0$表示母线平行于$z$轴的柱面

* **空间曲线的参数方程与一般方程**
    *    一般方程: $\begin{cases} F(x,y,z) = 0 \\ G(x,y,z) = 0 \end{cases}$
    *    参数方程: $\begin{cases} x = x(t) \\ y = y(t) \\ z = z(t) \end{cases}$
*   **二次曲面**:
    *   **椭球面**: $\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1$
        *   (图形描述：类似于一个椭圆在三维空间的扩展)
    *   **抛物面**:
        *   **椭圆抛物面**: $\frac{x^2}{a^2} + \frac{y^2}{b^2} = z$
            *   (图形描述：开口向上的碗状)
        *   **双曲抛物面**: $\frac{x^2}{a^2} - \frac{y^2}{b^2} = z$
            *   (图形描述：马鞍面)
    *   **双曲面**:
        *   **单叶双曲面**: $\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 1$
            *   (图形描述：类似于一个中间收缩的圆柱)
        *   **双叶双曲面**: $\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = -1$
            *   (图形描述：两个开口相对的碗状，不相交)
    *   **锥面**: $\frac{x^2}{a^2} + \frac{y^2}{b^2} - \frac{z^2}{c^2} = 0$
        *   (图形描述：圆锥)
    * **椭圆柱面**:$\frac{x^{2}}{a^{2}} + \frac{y^{2}}{b^{2}} = 1$
    * **双曲柱面**:$ \frac{x^{2}}{a^{2}} - \frac{y^{2}}{b^{2}} = 1$
    * **抛物柱面**: $y^{2} = 2px$
*   **空间曲线在坐标面上的投影**:
    *   空间曲线$\begin{cases} F(x,y,z) = 0 \\ G(x,y,z) = 0 \end{cases}$在$xOy$面上的投影曲线方程为$\begin{cases} H(x,y) = 0 \\ z=0 \end{cases}$, 其中$H(x,y)=0$通过原方程组消去$z$得到.

## 八. 其他

### 8.1. 欧拉积分
*    $\Gamma$ 函数: $\Gamma(s) = \int_{0}^{+\infty}x^{s-1}e^{-x}dx, s \gt 0$
     *   $\Gamma(s+1) = s\Gamma(s)$
     *   $\Gamma(n+1) = n!$
     *    $\Gamma(1) = 1, \Gamma(\frac{1}{2}) = \sqrt{\pi}$
     *   $\Gamma(s)\Gamma(1-s) = \frac{\pi}{sin\pi s}, 0 \lt s \lt 1$
*    $B$ 函数: $B(p,q) = \int_{0}^{1}x^{p-1}(1-x)^{q-1}dx = \int_{0}^{\frac{\pi}{2}}2sin^{2p-1}\theta cos^{2q-1}\theta d\theta$
    *    $B(p,q) = \frac{\Gamma(p)\Gamma(q)}{\Gamma(p+q)}$
    *   $B(p,q) = B(q,p)$

### 8.2. 多元函数微分(偏概念，求导，计算)

*   一阶偏导连续，可微，连续，二重极限存在之间的关系

    *   一阶偏导连续$\implies$可微$\implies$可偏导，连续$\implies$极限存在
    *   可微$\iff$可偏导且$\Delta z = f_x(x_0,y_0)\Delta x + f_y(x_0,y_0)\Delta y + o(\rho)$
*    可微的推导过程

      若函数$f(x,y)$在点$P_{0}(x_{0},y_{0})$的某邻域内有定义, 且函数在点$P_{0}$处的全增量
      $$\Delta z = f(x_{0} + \Delta x, y_{0} + \Delta y) - f(x_{0},y_{0})$$
      可以表示成
      $$\Delta z = A\Delta x + B\Delta y + o(\rho)$$
      其中$A$,$B$不依赖于$\Delta x$,$\Delta y$而仅与$x$,$y$有关,$\rho = \sqrt{(\Delta x)^{2} + (\Delta y)^{2}}$, 则称函数$f(x,y)$在点$P_{0}$处可微.

      证明充分性: 偏导连续$\implies$可微:
      利用微分中值定理，
      \begin{align}
      \Delta z &= f(x_{0} + \Delta x, y_{0} + \Delta y) - f(x_{0},y_{0}) \\
      &= f(x_0 + \Delta x, y_0 + \Delta y) - f(x_0, y_0 + \Delta y) + f(x_0, y_0 + \Delta y) - f(x_0, y_0) \\
      &= f_x(x_0 + \theta_1 \Delta x, y_0 + \Delta y)\Delta x + f_y(x_0, y_0 + \theta_2 \Delta y)\Delta y, (0 \lt \theta_1, \theta_2 \lt 1)
      \end{align}
      由于偏导数连续，所以
      \begin{align}
       \Delta z &= [f_x(x_0,y_0) + \alpha]\Delta x + [f_y(x_0,y_0) + \beta]\Delta y \\
      &= f_x(x_0,y_0)\Delta x + f_y(x_0,y_0)\Delta y + \alpha\Delta x + \beta\Delta y
      \end{align}
      其中,当$\Delta x \to 0, \Delta y \to 0$时,$\alpha \to 0, \beta \to 0$
      $$\because \lim_{\rho \to 0}\frac{\alpha \Delta x + \beta \Delta y}{\rho} = 0$$
      $$\therefore \alpha \Delta x + \beta \Delta y = o(\rho)$$
      $$\therefore \Delta z = f_x(x_0, y_0)\Delta x + f_y(x_0,y_0)\Delta y + o(\rho)$$
      因此$f(x,y)$在点$(x_0, y_0)$可微

      证明必要性: 可微$\implies$可偏导:
      由于$f(x,y)$在$(x_0,y_0)$处可微,则
      $$\Delta z = A\Delta x + B\Delta y + o(\rho)$$
      取$\Delta y = 0$, 有
      $$\Delta z = A\Delta x + o(|\Delta x|)$$
      从而有
      $$f_x(x_0,y_0) = \lim_{\Delta x \to 0}\frac{\Delta z}{\Delta x} = \lim_{\Delta x \to 0}\frac{A\Delta x + o(|\Delta x|)}{\Delta x} = A$$
      同理$f_y(x_0,y_0) = B$
*    全微分方程: $P(x,y)dx + Q(x,y)dy = 0$
    *   定义:如果存在二元函数$u=u(x,y)$, 使得$du(x,y) = P(x,y)dx + Q(x,y)dy$, 则称该方程为全微分方程。
    *   充要条件:$\frac{\partial P}{\partial y} = \frac{\partial Q}{\partial x}$
    *    $u = \int_{x_{0}}^{x}P(x,y_{0})dx + \int_{y_{0}}^{y}Q(x,y)dy$ 或 $u = \int_{x_{0}}^{x}P(x,y)dx + \int_{y_{0}}^{y}Q(x_{0},y)dy$
    *   $x,y$地位平等

### 8.3 概率论与数理统计

*    随机事件概率运算性质
    *    不可能事件$\phi$, 必然事件$\Omega$
    *    $A \subset B \implies P(A) \le P(B)$
    *    $P(A \cup B) = P(A) + P(B) - P(AB)$
        *   推广:
            *   $P(A \cup B \cup C) = P(A) + P(B) + P(C) - P(AB) - P(BC) - P(AC) + P(ABC)$
    *    $P(\bar A) = 1- P(A)$
    *   $P(A-B) = P(A\bar B) = P(A) - P(AB)$
    *   $P(AB) = P(A)P(B|A) = P(B)P(A|B)$
    *    对偶律: $\overline{A \cup B} = \bar{A} \cap \bar{B}; \overline{A \cap B} = \bar{A} \cup \bar{B}$
    *    独立性: $P(AB) = P(A)P(B)$
    *    全概率公式: $P(A) = \sum_{i=1}^{n}P(B_i)P(A|B_i)$
    *   贝叶斯公式: $P(B_i|A) = \frac{P(B_i)P(A|B_i)}{\sum_{j=1}^{n}P(B_j)P(A|B_j)}$
*    分布函数(连续+离散)
    *  定义: $F(x) = P(X \le x)$
    *  性质:
        *   单调不减
        *   右连续
        *   $0 \le F(x) \le 1$, $F(-\infty) = 0$, $F(+\infty) = 1$
    *   离散型: $F(x) = \sum_{x_k \le x}p_k$
    *   连续型: $F(x) = \int_{-\infty}^{x}f(t)dt$
*   几个重要的概率分布及其性质
    *   离散型
        *   0-1分布: $P(X=k) = p^k(1-p)^{1-k}, k=0,1$
        *   二项分布: $B(n,p)$, $P(X=k) = C_n^kp^k(1-p)^{n-k}, k=0,1,2,...,n$
            *    $EX=np, DX=np(1-p)$
        *   泊松分布: $P(\lambda)$, $P(X = k) = \frac{\lambda^ke^{-\lambda}}{k!}, k=0,1,2,...$
            *    $EX = \lambda, DX = \lambda$
        *   几何分布: $Ge(p)$, $P(X=k) = (1-p)^{k-1}p, k=1,2,3,...$
            *   $EX=\frac{1}{p}, DX = \frac{1-p}{p^2}$
            *   无记忆性
        *   超几何分布: $H(N,M,n)$,$P(X=k) = \frac{C_M^kC_{N-M}^{n-k}}{C_N^n}$
            *   $EX = \frac{nM}{N}$
    *   连续型
        *    均匀分布: $U(a,b)$,$f(x) = \begin{cases} \frac{1}{b-a}, & a \lt x \lt b \\ 0, & 其他 \end{cases}$
            *    $EX = \frac{a+b}{2}, DX = \frac{(b-a)^2}{12}$
        *    指数分布: $E(\lambda)$,$f(x) = \begin{cases} \lambda e^{-\lambda x}, & x \gt 0 \\ 0, & x \le 0 \end{cases}$
            *    $EX = \frac{1}{\lambda}, DX = \frac{1}{\lambda^2}$
            *   无记忆性
        *    正态分布: $N(\mu, \sigma^{2})$, $f(x) = \frac{1}{\sqrt{2\pi}\sigma}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$
            *   $EX = \mu, DX = \sigma^2$
            *   标准化: $X \sim N(\mu, \sigma^2) \implies \frac{X-\mu}{\sigma} \sim N(0,1)$
*   假设检验
    *    两类错误
        *   第一类错误($\alpha$): 弃真, $P$(拒绝$H_0$|$H_0$为真)
        *   第二类错误($\beta$): 取伪, $P$(接受$H_0$|$H_0$为假)
    *   显著性水平 ($\alpha$): 犯第一类错误的概率上限
    *   步骤:
        1.  提出原假设$H_0$和备择假设$H_1$.
        2.  选择检验统计量, 并在$H_0$成立的条件下确定其分布.
        3.  给定显著性水平$\alpha$, 确定临界值和拒绝域.
        4.  根据样本值计算检验统计量的值, 并做出判断.
    *    正态总体均值和方差的假设检验
*   参数估计
    *   点估计
        *   矩估计: 用样本矩估计总体矩
        *   最大似然估计: 找到使样本出现概率最大的参数值
    *   估计量的评选标准
        *   无偏性: $E(\hat{\theta}) = \theta$
        *   有效性: $D(\hat{\theta_1}) \lt D(\hat{\theta_2})$
        *   一致性 (相合性): $\hat{\theta_n} \xrightarrow{P} \theta$
    *   区间估计: 找到一个区间, 使总体参数以一定的概率落入该区间

### 8.4 线性代数

#### 8.4.1 行列式

*   **定义**: $n$ 阶行列式是由 $n^2$ 个数 $a_{ij}$ ($i, j = 1, 2, ..., n$) 排成的 $n$ 行 $n$ 列的数表，按照一定的规则进行运算得到的一个数。记作：
    $$D = \begin{vmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{n1} & a_{n2} & \cdots & a_{nn} \end{vmatrix}$$

*   **计算**:
    *   **二阶行列式**: $\begin{vmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{vmatrix} = a_{11}a_{22} - a_{12}a_{21}$
    *   **三阶行列式** (对角线法则):
        $\begin{vmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{vmatrix} = a_{11}a_{22}a_{33} + a_{12}a_{23}a_{31} + a_{13}a_{21}a_{32} - a_{13}a_{22}a_{31} - a_{11}a_{23}a_{32} - a_{12}a_{21}a_{33}$
    *   **n 阶行列式** (按行/列展开):
        *   **余子式**: 去掉 $a_{ij}$ 所在的第 $i$ 行和第 $j$ 列后剩下的 $(n-1)$ 阶行列式，记作 $M_{ij}$。
        *   **代数余子式**: $A_{ij} = (-1)^{i+j} M_{ij}$
        *   **按行展开**: $D = a_{i1}A_{i1} + a_{i2}A_{i2} + ... + a_{in}A_{in}$
        *   **按列展开**: $D = a_{1j}A_{1j} + a_{2j}A_{2j} + ... + a_{nj}A_{nj}$
    *    **特殊行列式**
        *    上(下)三角行列式: 对角线下方(上方)元素全为0
        *    对角行列式:  除了主对角线上的元素外，其他元素都为0
        *    范德蒙德行列式
        *    分块行列式

*   **性质**:
    *   行列式与它的转置行列式相等: $|A| = |A^T|$
    *   互换行列式的两行 (列)，行列式变号。
    *   行列式的某一行 (列) 的所有元素同乘以数 $k$，等于用数 $k$ 乘此行列式。
    *   行列式中如果有两行 (列) 元素成比例，则此行列式为零。
    *   若行列式的某一列 (行) 的元素都是两数之和，则此行列式等于对应的两个行列式之和。
    *   把行列式的某一列 (行) 的各元素乘以同一数然后加到另一列 (行) 对应的元素上去，行列式不变。
    *    $|kA| = k^n|A|$
    *    $|AB| = |A||B|$
    *    $|A^*| = |A|^{n-1}$

* **克拉默法则**:
    *   如果线性方程组的系数行列式 $D \ne 0$，则方程组有唯一解：
        $x_1 = \frac{D_1}{D}, x_2 = \frac{D_2}{D}, ..., x_n = \frac{D_n}{D}$
        其中 $D_j$ 是把系数行列式 $D$ 中第 $j$ 列的元素用方程组右端的常数项代替后得到的 $n$ 阶行列式。
    *    齐次线性方程组有非零解的充要条件是系数行列式为0。

#### 8.4.2 矩阵

*   **定义**: 由 $m \times n$ 个数 $a_{ij}$ ($i = 1, 2, ..., m$; $j = 1, 2, ..., n$) 排成的 $m$ 行 $n$ 列的数表，称为 $m \times n$ 矩阵，记作：
    $$A = \begin{pmatrix} a_{11} & a_{12} & \cdots & a_{1n} \\ a_{21} & a_{22} & \cdots & a_{2n} \\ \vdots & \vdots & \ddots & \vdots \\ a_{m1} & a_{m2} & \cdots & a_{mn} \end{pmatrix}$$

*   **特殊矩阵**:
    *   **零矩阵**: 所有元素都为 0 的矩阵。
    *   **方阵**: 行数和列数相等的矩阵。
    *   **单位矩阵**: 主对角线元素为 1，其他元素为 0 的方阵，记作 $E$ 或 $I$。
    *   **对角矩阵**: 除了主对角线上的元素外，其他元素都为 0 的方阵。
    *   **上 (下) 三角矩阵**: 主对角线下 (上) 方的元素都为 0 的方阵。
    *   **对称矩阵**: $A^T = A$
    *   **反对称矩阵**: $A^T = -A$
    *   **正交矩阵**: $A^T A = A A^T = E$
    *    **数量矩阵**: $kE$

*   **矩阵运算**:
    *   **加法**: 同型矩阵才能相加，$A + B = (a_{ij} + b_{ij})$
    *   **数乘**: $kA = (ka_{ij})$
    *   **乘法**: $A$ 的列数等于 $B$ 的行数时，$AB$ 才有意义。$(AB)_{ij} = \sum_{k=1}^n a_{ik}b_{kj}$
        *   不满足交换律: $AB \ne BA$ (一般情况下)
        *   满足结合律: $(AB)C = A(BC)$
        *   满足分配律: $A(B+C) = AB + AC$, $(A+B)C = AC + BC$
        *   $AE = EA = A$
        *   $(AB)^T = B^T A^T$
        *    $(AB)^{-1} = B^{-1}A^{-1}$
        *    $(AB)^* = B^*A^*$
    *   **转置**: $(A^T)^T = A$, $(A+B)^T = A^T + B^T$, $(kA)^T = kA^T$, $(AB)^T = B^T A^T$
    *   **逆**:
        *   定义: 若存在矩阵 $B$，使得 $AB = BA = E$，则称 $A$ 可逆，$B$ 为 $A$ 的逆矩阵，记作 $A^{-1}$。
        *   $A$ 可逆 $\Leftrightarrow$ $|A| \ne 0$
        *   $A^{-1} = \frac{1}{|A|} A^*$ (其中 $A^*$ 为 $A$ 的伴随矩阵)
        *   $(A^{-1})^{-1} = A$
        *   $(kA)^{-1} = \frac{1}{k} A^{-1}$
        *   $(AB)^{-1} = B^{-1}A^{-1}$
        *   $(A^T)^{-1} = (A^{-1})^T$
    * **伴随矩阵**
      * 定义: $A^* = (A_{ij})^{T}$, 即$A$的代数余子式构成的矩阵的转置
      * $AA^* = A^*A = |A|E$
    *   **矩阵的幂**: $A^k = \underbrace{A \cdot A \cdot ... \cdot A}_{k 个}$
    *   **方阵的多项式**: $f(A) = a_0 E + a_1 A + a_2 A^2 + ... + a_n A^n$
*    **分块矩阵**

*   **矩阵的初等变换**:
    *   交换矩阵的两行 (列)
    *   用非零常数 $k$ 乘以矩阵的某一行 (列)
    *   把矩阵的某一行 (列) 的 $k$ 倍加到另一行 (列)
    *    初等行变换与初等列变换统称初等变换.
    *   初等矩阵: 单位矩阵经过一次初等变换得到的矩阵
    *    初等变换不改变矩阵的秩.

*   **矩阵的秩**:
    *   定义: 矩阵 $A$ 中非零子式的最高阶数，记作 $r(A)$。
    *   $r(A) = r$ $\Leftrightarrow$ $A$ 中有 $r$ 阶子式不为 0，且所有 $r+1$ 阶子式 (如果存在) 都为 0。
    *   性质:
        *   $r(A) = r(A^T)$
        *   $r(kA) = r(A)$ ($k \ne 0$)
        *   $r(A+B) \le r(A) + r(B)$
        *   $r(AB) \le \min\{r(A), r(B)\}$
        *    $r(A) + r(B) - n \le r(AB)$, 其中$A$是$m \times n$矩阵, $B$是$n \times s$矩阵.
        *   若 $A$ 可逆，则 $r(AB) = r(B)$；若 $B$ 可逆，则 $r(AB) = r(A)$。
        *   $r(A^TA) = r(AA^T) = r(A)$
        *   $max\{r(A), r(B)\} \le r(A, B) \le r(A) + r(B)$
        *   $r(\begin{pmatrix} A & O \\ O & B \end{pmatrix}) = r(A) + r(B)$

#### 8.4.3 向量组

* **n维向量**: n个数组成的有序数组

*   **向量组的线性组合、线性表示、线性相关、线性无关** (定义同 7.1)
* **向量组的等价**
    *   定义: 两个向量组可以相互线性表示
    *   性质:
        *   等价的向量组有相同的秩
        *   等价的向量组所含向量的个数可以不同.

*   **向量组的秩**:
    *   定义: 向量组的极大线性无关组所含向量的个数。
    *   $r(\alpha_1, \alpha_2, ..., \alpha_s) = r$ $\Leftrightarrow$ 向量组中有 $r$ 个向量线性无关，且任意 $r+1$ 个向量 (如果存在) 都线性相关。

*   **向量空间**:
    *   定义: 向量组的线性组合构成的集合。
    *   **基**: 向量空间的一组线性无关的向量，且该向量空间中的任意向量都可由这组向量线性表示。
    *   **维数**: 基中所含向量的个数。

#### 8.4.4 线性方程组

*   **n 元线性方程组**:
    $$\begin{cases} a_{11}x_1 + a_{12}x_2 + ... + a_{1n}x_n = b_1 \\ a_{21}x_1 + a_{22}x_2 + ... + a_{2n}x_n = b_2 \\ \cdots \cdots \cdots \cdots \cdots \cdots \cdots \cdots \cdots \\ a_{m1}x_1 + a_{m2}x_2 + ... + a_{mn}x_n = b_m \end{cases}$$

*   **矩阵表示**: $Ax = b$ (其中 $A$ 为系数矩阵，$x$ 为未知数向量，$b$ 为常数项向量)

*   **解的判定**:
    *   **无解**: $r(A) \ne r(A, b)$
    *   **唯一解**: $r(A) = r(A, b) = n$
    *   **无穷多解**: $r(A) = r(A, b) < n$
*   **齐次线性方程组** $Ax=0$
    *   有非零解的充要条件是$r(A) \lt n$
    *   基础解系: 齐次线性方程组的线性无关的解向量, 且方程组的任意解都可以由基础解系线性表示.
    *   基础解系所含向量个数: $n-r(A)$
    *   通解: $k_1\xi_1 + k_2\xi_2 + ... + k_{n-r(A)}\xi_{n-r(A)}$
*   **非齐次线性方程组**$Ax = b$
    *   解的结构: 特解 + 对应齐次方程组的通解
    *   特解的求法:
        *   观察法
        *   初等行变换法
#### 8.4.5 特征值与特征向量
* **定义**
    *   对于n阶方阵$A$, 若存在数$\lambda$和非零向量$\alpha$, 使得$A\alpha = \lambda\alpha$成立, 则称$\lambda$为方阵$A$的特征值, 非零向量$\alpha$为$A$的对应于特征值$\lambda$的特征向量.
*    **特征值与特征向量的求法**:
    1.  计算特征多项式: $| \lambda E - A |$
    2.  求出特征方程 $| \lambda E - A | = 0$ 的根, 即为特征值.
    3.  对每个特征值 $\lambda$, 解方程组 $(\lambda E - A)x = 0$, 得到非零解, 即为对应的特征向量.
* **性质**
    *   $A$和$A^{T}$有相同的特征值
    *   $tr(A) = \sum_{i=1}^{n}\lambda_i = \sum_{i=1}^{n}a_{ii}$
    *   $|A| = \prod_{i=1}^{n}\lambda_i$
    *   不同特征值的特征向量线性无关.
    *   k重特征值至多有k个线性无关的特征向量.
    *    若$A\alpha = \lambda\alpha$, 则
         *    $kA\alpha = (k\lambda)\alpha$
         *    $A^{m}\alpha = \lambda^{m}\alpha$
         *   $f(A)\alpha = f(\lambda)\alpha$
         *   $A^{-1}\alpha = \frac{1}{\lambda}\alpha$
         *   $A^{*}\alpha = \frac{|A|}{\lambda}\alpha$

#### 8.4.6 矩阵的相似对角化

*   **定义**: 若存在可逆矩阵 $P$，使得 $P^{-1}AP = \Lambda$ (其中 $\Lambda$ 为对角矩阵)，则称 $A$ 可相似对角化。
* **相似对角化的条件**
    *   $A$有n个线性无关的特征向量.
    *   $A$的每个k重特征值有k个线性无关的特征向量.
    *   $A$为实对称矩阵
*    **性质**
    *    相似的矩阵具有相同的特征值，特征多项式，行列式， 迹，秩
    *    $A \sim B \implies A^{m} \sim B^{m}$
    *    $A \sim B \implies f(A) \sim f(B)$
    *   $A \sim B \implies A^{-1} \sim B^{-1}$ (若$A$,$B$可逆)
    *   $A \sim B \implies A^{T} \sim B^{T}$
    *   $A \sim B \implies A^{*} \sim B^{*}$

#### 8.4.7 二次型

*   **定义**: $n$ 个变量的二次齐次多项式
    $$f(x_1, x_2, ..., x_n) = \sum_{i=1}^n \sum_{j=1}^n a_{ij}x_i x_j$$
    其中 $a_{ij} = a_{ji}$。

*   **矩阵表示**: $f(x) = x^T A x$ (其中 $A$ 为对称矩阵)

*   **标准形**: 只含平方项的二次型 ($f(x) = d_1 y_1^2 + d_2 y_2^2 + ... + d_n y_n^2$)

*   **规范形**: 系数为 1, -1 或 0 的标准形

*   **二次型的标准化**:
    *   **配方法**
    *   **正交变换法**:
        1.  求出 $A$ 的特征值 $\lambda_1, \lambda_2, ..., \lambda_n$。
        2.  求出 $A$ 的对应于每个特征值的特征向量。
        3.  将特征向量正交化、单位化，得到正交向量组 $\eta_1, \eta_2, ..., \eta_n$。
        4.  构造正交矩阵 $Q = (\eta_1, \eta_2, ..., \eta_n)$。
        5.  则 $Q^T A Q = \Lambda = \begin{pmatrix} \lambda_1 & & \\ & \ddots & \\ & & \lambda_n \end{pmatrix}$，且 $f(x) = x^T A x = y^T \Lambda y = \lambda_1 y_1^2 + \lambda_2 y_2^2 + ... + \lambda_n y_n^2$，其中 $x = Qy$。

*   **惯性定理**: 二次型的标准形不唯一，但标准形中所含的正平方项个数和负平方项个数是唯一确定的。

*   **正定二次型**:
    *   定义: 若对任意 $x \ne 0$，都有 $f(x) = x^T A x > 0$，则称 $f(x)$ 为正定二次型，$A$ 为正定矩阵。
    *   判别方法:
        *   $A$ 的特征值全大于 0。
        *   $A$ 的顺序主子式全大于 0。
        *   $A$ 合同于单位矩阵 $E$。
        *   存在可逆矩阵$P$, 使得$A = P^{T}P$
    *    性质
        *   正定矩阵的行列式大于0
        *   正定矩阵的主对角线上的元素大于0
        *   正定矩阵的逆矩阵也是正定的
        *    正定矩阵的和仍是正定的
        *    正定矩阵与正定矩阵的乘积不一定是正定矩阵

*   **矩阵的合同**:
    *   定义: 若存在可逆矩阵 $C$，使得 $C^T A C = B$，则称矩阵 $A$ 与 $B$ 合同。
    *    性质
         *   合同的矩阵具有相同的秩
         *    合同的矩阵具有相同的正负惯性指数
         *    合同的矩阵具有相同的正定性