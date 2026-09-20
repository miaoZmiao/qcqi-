1 全貌
量子力学是 一个 数学框架 或 物理理论构建的规则集

应用与认知 并行 --> 量子计算 & 量子信息

1.2量子比特

特定属性的数学对象

单个量子比特 两个状态，用狄拉克符号包起来
 \(\vert{}\psi\rangle\)

0 和 1 变成
\(\vert{}0\rangle\) 和 \(\vert{}1\rangle\)
1) 右矢 (Ket): 表示系统的量子状态 (列向量)
   - 符号: |ψ⟩
   - 读作: Ket psi / 右矢 psi / ψ 态
   - 计算基态:
     * |0⟩ : Ket zero / 右矢 0 / 0 态 (对应经典 0)
     * |1⟩ : Ket one  / 右矢 1 / 1 态 (对应经典 1)

2) 左矢 (Bra): 右矢的共轭转置 (行向量)
   - 符号: ⟨ψ|
   - 读作: Bra psi / 左矢 psi

3) 内积 (Bra-Ket / Bracket):
   - 符号: ⟨φ|ψ⟩
   - 物理意义: 两个量子态之间的重叠程度 / 概率幅。

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

在这里存疑
疑问1 ： Uf 的数学表达式
疑问2 ： 实际测量的是什么

3 量子算法总结
 1 基于傅里叶的量子算法？？  
       n * 2^n - >  n^2
 2 量子搜索
       N  -> 根号N
 3 量子模拟
      c^n -> k * n


1.5 实验量子信息处理

1 stern-gerlach 实验 
  1 自旋 只有 两级 
   ------- 理解这个实验很重要： 这个实验把 1 个量子比特系统， 对应一个 2 维   向量 来描述其量子态 AND 2 维   变化矩阵 说明白了
                    由这个实验延伸出      N 个量子比特系统， 对应一个 2^N 维 向量        量子态 AND 2^N 维 演化矩阵
2 实用量子信息前景
   量子处理途径：
   1 囚禁不同原子： 离子阱
   2 核磁共振：  噪声大

1.6 量子信息
广义： 凡事 量子力学 处理的信息 ： 量子计算，量子算法，量子 XXXX
狭义：量子信息理论， 研究 信息本身 在 量子力学下的基本规律

量子信息理论：
1 静态资源： 量子比特
2 动力学过程： 怎么传输，怎么抗噪
3 资源折中： 怎么用最小的资源成本，完成信息传输

描述经典问题：传输经典比特，传多快，需要多少纠错码
传输量子比特：压缩很难，只能从保真度（Fidelity） 下手
量子可区分性：非正交量子态 是 不可区分的
                      书上例子是区分  $\vert{}0\rangle$ 和 $\frac{\vert{}0\rangle+\vert{}1\rangle}{\sqrt{2}}$

量子纠缠提出问题：1 纠缠怎么产生 2 纠缠怎么转化


1.6.2 更广泛背景下的量子信息

核心定位：第一章总结，引导后续第 11 章（熵）与第 12 章（纯量子信息理论）。

三大根本追问：
1. 究竟是什么赋予了量子信息处理强大的能力？
2. 量子世界与经典世界的物理边界在哪里？
3. 量子计算利用的核心非经典资源是什么？（如叠加态、纠缠态、相干干涉）

