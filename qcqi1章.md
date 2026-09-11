1 全貌
量子力学是 一个 数学框架 或 物理理论构建的规则集

应用与认知 并行 --> 量子计算 & 量子信息

1.2量子比特

特定属性的数学对象

单个量子比特 两个状态，用狄拉克符号包起来
 \(\vert{}\psi\rangle\)

0 和 1 变成
\(\vert{}0\rangle\) 和 \(\vert{}1\rangle\)

量子比特是状态的线性组合(叠加态)
$|\psi\rangle = \alpha|0\rangle + \beta|1\rangle$

$\alpha, \beta \in \mathbb{C}$
满足约束：
$|\alpha|^2 + |\beta|^2 = 1$

我们无法知道了 $\alpha, \beta$，
但是通过测量知道 $|\alpha|^2, |\beta|^2$ ，即检测到 $|0\rangle$ 和 $|1\rangle$ 的概率。

量子比特的另一个描述 是 布洛赫球

$|\psi\rangle = e^{i\gamma} \left( \cos\frac{\theta}{2}|0\rangle + e^{i\varphi} \sin\frac{\theta}{2}|1\rangle \right)$

我们可以忽略全局相位因子 $e^{i\gamma}$，因此公式可以简化为：

$|\psi\rangle = \cos\frac{\theta}{2}|0\rangle + e^{i\varphi} \sin\frac{\theta}{2}|1\rangle$

$\theta$ $\varphi$ $\gamma$ 都是实数

$\theta$ 写作 \theta
$\varphi$ 写作 \varphi
$\gamma$ 写作 \gamma
$\psi$ 写作 \psi

多量子比特
首先模拟要用的状态就 是 $2^N$ ,N是量子比特数量
比如 N = 2，那就有 4 个基矢量：
$|00\rangle, |01\rangle, |10\rangle, |11\rangle$
描述两个量子比特态向量：
$|\psi\rangle = \alpha_{00}|00\rangle + \alpha_{01}|01\rangle + \alpha_{10}|10\rangle + \alpha_{11}|11\rangle$
满足约束条件：
$\displaystyle \sum_{x \in \{0, 1\}^2} |\alpha_x|^2 = 1$

1.3 量子计算

单比特量子门
重要性质：酉矩阵, $X^\dagger X = I$
常见的门：
Z门：
$Z = \begin{bmatrix} 1 & 0 \\ 0 & -1 \end{bmatrix}$
非门：
$X = \begin{bmatrix} 0 & 1 \\ 1 & 0 \end{bmatrix}$
H门：
$H = \frac{1}{\sqrt{2}} \begin{bmatrix} 1 & 1 \\ 1 & -1 \end{bmatrix}$
任意单比特门 都可以分解为：
$U = e^{i\alpha} \begin{bmatrix} e^{-i\beta/2} & 0 \\ 0 & e^{i\beta/2} \end{bmatrix} \begin{bmatrix} \cos\frac{\gamma}{2} & -\sin\frac{\gamma}{2} \\ \sin\frac{\gamma}{2} & \cos\frac{\gamma}{2} \end{bmatrix} \begin{bmatrix} e^{-i\delta/2} & 0 \\ 0 & e^{i\delta/2} \end{bmatrix}$

ZYZ欧拉角分解

多量子比特门
例子 CNOT 门
$U_{\text{CNOT}} = \begin{bmatrix} 1 & 0 & 0 & 0 \\ 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 1 \\ 0 & 0 & 1 & 0 \end{bmatrix}$

一般结论：测量的基可以任选，毕竟 变化矩阵保证 酉 性 就可以

量子电路
1 电路没法复制
2 贝尔态 = 阿达玛H  + CNOT 门

1.4  量子算法

量子计算机
1 可以实现经典电路门
   Toffoli 门 可以 模拟 NAND 门
2 计算可以并行
Deutsch 算法

Deutsh-Jozsa 算法  -- 我称之为猜函数 游戏
这个有好多细节要理解

