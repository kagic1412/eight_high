# 1 内生增长
## 1.1两部门模型
### Goods-producing sector
$$ Y(t) = [(1-a_K)K(t)]^\alpha [A(t)(1-a_L)L(t)]^{1-\alpha} $$
• $Y(t)$：产出 (Output)。即$t$时刻经济体生产的最终产品总量。

• $K(t)$：总资本存量 (Total Capital Stock)。整个经济体在$t$时刻拥有的资本总量。

• $L(t)$：总劳动力 (Total Labor)。整个经济体在$t$时刻拥有的劳动力总量。

• $A(t)$：知识存量/技术水平 (Stock of Knowledge)。代表当前的生产技术效率。在这里它以"劳动增强型"（Labor-augmenting）的方式进入生产函数。

• $a_K$：分配给研发的资本比例。因此，$(1-a_K)$ 是分配给产品生产的资本比例。这是一个外生参数（在基础R&D模型中），取值在0到1之间。

• $a_L$：分配给研发的劳动力比例。因此，$(1-a_L)$ 是分配给产品生产的劳动力比例。

• $\alpha$：资本的产出弹性 (Output Elasticity of Capital)。反映资本在产品生产中的贡献份额，取值通常在 $0<\alpha<1$ 之间。

• $1-\alpha$：有效劳动的产出弹性。反映有效劳动（包含技术进步的劳动）在生产中的份额。
### R&D sector
$$\frac{dA(t)}{dt} = B[a_K K(t)]^\beta [a_L L(t)]^\gamma A(t)^\theta$$
$\dot{A}(t)$：知识的增量 (Change in Knowledge)。即 $\frac{dA(t)}{dt}$，代表新产生的知识或技术的数量。

• $B$：研发部门的生产率参数 (Shift Parameter)。代表研发活动的整体效率，$B>0$。

• $a_K K(t)$：研发资本投入。即分配给研发部门使用的那部分资本。

• $a_L L(t)$：研发劳动力投入。即分配给研发部门的研究人员数量。

• $\beta$：研发中资本的产出弹性。反映资本投入对新知识产生的贡献度，$\beta \geq 0$。

• $\gamma$：研发中劳动力的产出弹性。反映科研人员数量对新知识产生的贡献度，$\gamma \geq 0$。

• $\theta$：现有知识存量的溢出效应参数 (Effect of existing knowledge)。这是一个非常关键的参数：

- 反映了"站在巨人的肩膀上"效应。即现有的知识 $A(t)$对研发新知识 $\dot{A}(t)$ 的帮助程度。
- 如果 $\theta>0$ ，表示现有知识越多，研发越容易（正外部性）。
- 如果 $\theta<0$，表示"钓鱼效应"（Fishing-out effect），即简单的发明都被发现了，剩下的越来越难。
- 在基础模型讨论中，$\theta$ 的取值（是否等于、大于或小于1）决定了经济增长是否收敛或爆炸

## 1.2 无资本动态的模型（Simple Version: Without）
- 产品部门
$$ Y(t) = A(t)(1-a_L)L(t) $$
- 研发部门
$$\frac{dA(t)}{dt} = B [a_L L(t)]^\gamma A(t)^\theta$$
### Dynamics of A
- 研发部门
    $$g_A(t) = \frac{\dot{A}(t)}{A(t)} = B[a_L L(t)]^\gamma A(t)^{\theta - 1}$$
    $$\dot{g}_A(t) = \gamma n g_A(t) + (\theta - 1)[g_A(t)]^2$$
- 生产部门
    $$Y(t) = A(t)(1 - a_L)L(t)$$
    $$g_Y/L(t) = g_A(t)$$
    
###  核心分析：θ 决定增长命运
- 情况 1: $\theta<1$ （收敛 / 半内生增长）

    这是最接近传统直觉的情况，意味着随着知识存量的增加，产生新知识的难度加大（边际报酬递减）。

    收敛性： 知识增长率 g_A，最终会收敛到一个由人口增长率 n 决定的稳态值：  $$g^*_A = \frac{\gamma n}{1-\theta}$$

 
    这表明，如果 $\theta<1$，长期增长依然依赖于外生的人口增长（n），这被称为“半内生增长”（Semi-endogenous growth）。

   政策无效性（仅有水平效应）： 如果政府通过政策永久性地增加了研发人员比例 $a_
L$，并不能永久性地提高长期增长率。它只能带来暂时的增长加速，随后增长率会回落到 $g_A^∗$
​
 。这种现象被称为水平效应（Level Effect），而非增长效应。
- 情况 2: $\theta>1$ （爆炸性增长）

    如果现有知识对新知识产生的促进作用非常强（规模报酬递增），经济将进入发散路径。
    动态特征： 根据知识增长率的动态方程，增长率将随着时间推移不断加速：$$\dot{g}_A(t) = \gamma n g_A(t) + (\theta - 1)[g_A(t)]^2 > 0$$

    结果： 除非受到其他约束，这种参数设置会导致数学上的“爆炸”（Explosive growth），即增长率趋向于无穷大，这在现实中较难维持,。
- 情况 3: $\theta =1$ （真正的内生增长）

    这是内生增长理论最关注的“刀锋”情况，即现有知识对新知识产生的贡献是线性的（恒定规模报酬）。
    稳态增长： 假设人口不增长 (n=0)，经济从一开始就处于稳定的增长路径上，其增长率由研发投入直接决定：$$g_A = B[a_L L]^\gamma$$

- 政策有效性（增长效应）： 此时，增加研发投入比例 a_ L
  可以永久性地提高长期增长率。这正是内生增长理论试图证明的结论——内部政策可以改变长期增长率。

### 人口的作用
- 该简化模型还得出一个与Solow模型截然不同的结论：人口增长对经济增长有正向影响。

    机制： 在Solow模型中，人口增长会稀释资本，降低人均收入；但在R&D模型中，人是生产知识的关键投入（Researchers）。更多的人意味着更快的知识积累，从而推动增长,。


## 1.3 有资本动态的一般模型（Model with Capital Dynamics）
### 资本动态
- 推导
 $$\dot{K}(t) = sY(t)$$
 生产部门生产函数
 $$ Y(t) = [(1 - a_K) K(t)]^{\alpha} [A(t) (1 - a_L) L(t)]^{1-\alpha}$$
   $$ g_K(t) = \frac{\dot{K}(t)}{K(t)} = c_K K(t)^{\alpha-1} A(t)^{1-\alpha} L(t)^{1-\alpha}$$
   其中$ c_k $ 是包含储蓄率和资源分配比例的常数项$$\quad c_K = s(1 - a_K)^\alpha (1 - a_L)^{1-\alpha}$$
- 为了分析动态路径，我们需要看 $g_K$随时间是如何变化的。资料给出了$ g_K$变动的核心方程
 $$\frac{\dot{g}_K(t)}{g_K(t)} = (1 - \alpha)[g_A(t) + n - g_K(t)]$$

### 知识动态
- 核心方程

    研发部门不仅使用劳动力 (L) 和现有知识 (A)，还使用资本 (K)（如实验室设备、计算机等）。
    $$\dot{A} = B[a_K K]^{\beta}[a_L L]^{\gamma} A^\theta$$
    知识增长率动态方程
    $$\frac{\dot g_A(t)}{g_A(t)} = \beta g_K(t) + \gamma n + (\theta - 1) g_A(t)$$
    - $\beta g_K(t)$:（资本助推）： 资本积累速度越快，研发设备更新越快，推动知识增长率上升。
    - $\gamma n$:（人口红利）： 人口增长提供更多的研究人员，推动增长。
    - $(\theta - 1) g_A(t)$:（知识难度的反馈）： 如果 $\theta<1$，随着 $g_A$
  增加，进一步创新的难度加大，会拖累增长率；如果 $\theta>1$，则会形成正反馈加速。

### 模型最终命运
- 虽然资本动态本身具有稳定性（总是试图追赶 $g_A+n $ ），但整个经济的最终命运取决于它与知识动态 ( $g_A$ ) 的互动，具体由参数 $ \beta+\theta $ 决定
- 收敛情况 ($ \beta+\theta $<1)

    知识增长率 $g_A$也会稳定下来。资本增长率最终会收敛到一个常数稳态： 
   $$ g_K^* = g_A^* + n = \frac{\gamma n}{1 - (\beta + \theta)} + n$$
   此时，资本积累和知识积累达到了同步的恒定速度
- 内生增长情况 ($\beta+\theta=1,n=0$)： 

    资本和知识形成完美的互补。在平衡增长路径（BGP）上，两者以相同的速率增长：$g
   _K=g_A$。此时储蓄率 $s$ 的增加可以直接提升 $g_K$，进而永久提升 $g_A$
- 爆炸情况 ($\beta+\theta>1$)

     虽然资本总想追赶 $g_A+n$，但由于 $\beta$ (资本对研发的贡献) 和 $\theta$ (知识溢出) 很大, 资本的积累会反过来推高 $g_A$，而更高的 $g_A$ 又要求更高的 $g_K$。 因此, $g_K$ 始终无法追上均衡线，而是被 $g_A$ 拖着一同进入“双爆炸”区域，两者的增长率都持续上升 ($\dot g_K > 0$ 且 $\dot g_A > 0$)。

## 1.4 R&D资源分配
    在内生增长模型（特别是R&D模型）R&D资源分配与微观基础的讨论主要集中在“为什么要进行研发”、“市场如何分配资源”以及“这种分配是否有效”这三个核心问题上。
### 资源分配的动因:知识的本质与市场失灵
- 在基础R&D模型中，研发投入比例（$a_L,a_K$）通常被假设为外生的固定参数。然而，探讨其微观基础旨在解释这些资源分配背后的经济动机。资料指出，这面临一个核心矛盾.
- 知识的非竞争性 (Non-rivalry)： 知识一旦产生，一个人使用它并不会妨碍其他人使用。在完全竞争市场中，非竞争性商品的价格应趋向于边际成本（即零）
- 激励缺失： 如果价格为零，私人在完全竞争市场中就没有动机去进行研发。因此，为了激励R&D活动，模型必须引入不完全竞争（如专利带来的市场势力）、政府支持或外部性（如干中学）
### 分配机制案例：干中学（Learning-by-Doing）与AK模型
- 核心定位：解决“激励缺失”的另一条路径
- 模型机制：作为“副产品”的知识
    - $$Y(t) = K(t)^\alpha [A(t)L(t)]^{1-\alpha}$$
    厂商在积累资本（K）的过程中，无意间获得了很多经验，提升了技术水平（A）
    - $$A(t) = BK(t)^\phi$$
- Dynamics of K
    $$\dot{K}(t) = sK(t)^\alpha [A(t)L(t)]^{1-\alpha} $$
    $$= sK(t)^\alpha [BK(t)^\phi L(t)]^{1-\alpha} $$
    $$= sB^{1-\alpha}L(t)^{1-\alpha}K(t)^{\alpha+\phi(1-\alpha)}$$
- Growth Rate of K
   $$ \dot{K}(t) = sB^{1-\alpha}L(t)^{1-\alpha}K(t)^{\alpha+\phi(1-\alpha)}$$
  $$ g_K(t) = \frac{\dot{K}(t)}{K(t)} = sB^{1-\alpha}L(t)^{1-\alpha}K(t)^{\alpha+\phi(1-\alpha)-1}$$
  $$\dot{g}_K(t) = (1-\alpha)ng_K(t) + (\alpha+\phi(1-\alpha)-1)[g_K(t)]^2$$
- 演化条件
    当参数 $\phi=1 $且人口增长 $n$=0 时，模型中的生产函数$$Y(t) = K(t)^\alpha [A(t)L(t)]^{1-\alpha}$$实际上就变成了 AK模型 ($Y=\tilde A k$)
    - 这解释了AK模型中“资本边际报酬不变”的来源——虽然单个厂商面临资本边际报酬递减（$\alpha$<1），但加上全社会的知识溢出（干中学），总体回报率变成了常数。
- 资源分配的低效性：私人 vs. 社会(推导过程略)
    - 私人视角（竞争性均衡）

    单个厂商（$Firm_j$）无法控制全社会的知识水平 A(t)，它将其视为外生变量。
    厂商决策时只考虑私人的资本回报率：$$r_{EQ} = \alpha (BL)^{1-\alpha}$$
    厂商只看到了自己投资带来的直接产出（$\alpha$ 部分），忽略了自己投资对全社会技术进步的贡献 $\phi$。
    - 社会视角（帕累托最优）
    社会计划者（Social Planner）知道增加资本$ K $会同步提升$ A$（因为 $A = BK^\phi$）。
    社会视角的真实资本回报率包含了技术溢出：$$r_{PE} = (BL)^{1-\alpha}$$
    由于 $\alpha < 1$，显然 私人回报 < 社会回报。
# 2 romer 模型
## 2.1 模型概述与基本假设
- Romer模型的核心思想是：研发（R&D）驱动增长，而增长反过来影响研发的激励
- 垄断权利：为了解决我们之前讨论的“价格为零”导致“激励缺失”的问题，Romer模型假设想法的开发者拥有永久的垄断权（专利）。这允许他们设定高于成本的价格，从而获得利润来覆盖研发成本
### 2.2 核心假设：简化的宏观环境
- 参数设定： 假设 θ=1 且人口增长 n=0
- 含义： 这意味着不需要考虑过渡动态（Transition dynamics），经济直接处于平衡增长路径上。这属于真正的内生增长情形，即知识积累对现有知识存量呈线性关系。
### 2.3具体部门假设与生产函数
- 研发与中间产品部门（R&D Sector）
    - 生产函数（知识积累）： $$\dot{A} = B L_A A$$
    - 市场结构： 研发部门是**自由进入（Free Entry**的，意味着任何人都可以雇佣劳动来发明新想法，直到预期利润净现值等于研发成本
- 最终产品部门（Final Goods Sector）
    - 行为： 代表性厂商收集所有可用的专业化中间投入品 $L(i)$ 来生产最终产出 $Y$
    - $$Y(t) = \left[ \int_0^{A(t)} L(i, t)^\phi di \right]^{1/\phi} , \quad 0 < \phi < 1$$
    $\phi$ 衡量了不同中间投入品 L(i) 之间的替代程度,越接近 1，中间品之间的替代性越强,越接近 0，中间品之间的替代性越弱

    这个函数体现了“对样数（variety）的偏好”。

    如果利用对称性（即所有中间品使用量相同），该函数可以简化为：$$Y(t) = A(t)^{(1-\phi)/\phi}L_Y(t)$$这表明，产出不仅取决于生产工人 $L_Y$，还随着知识种类 $A$ 的增加而增加（规模报酬递增）。

- 劳动力市场
    - 假设人口固定： 总人口 $\bar{L}$ 是固定的（对应 $n=0$）。
    - 资源分配： 人口被划分为两部分：一部分搞研发 ($L_A$)，一部分搞生产 ($L_Y$)。$$\bar{L} = L_A(t) + L_Y(t)$$
    - 完全竞争： 劳动力市场是完全竞争的，这意味着研发部门和生产部门支付的工资 $w(t)$ 必须相等。
- 家庭部门（Households）
    - 效用最大化： 类似于Ramsey-Cass-Koopmans (RCK) 模型，代表性家庭追求跨期效用最大化：
    $$U = \int_0^{\infty} e^{-\rho t} \ln C(t) dt$$
    -  Subject to a lifetime constraint:
    $$\int_0^\infty e^{-rt} C(t)dt = X(0) + \int_0^\infty e^{-rt} w(t)dt$$
    - 其中 $\rho$ 是贴现率。家庭面临预算约束，其消费决策决定了储蓄和资本供给（在本模型中简化为资源在即期消费与投资新知识之间的权衡）。
    - $X(0)$ is the initial wealth per person.
    - $r$ is the interest rate. We consider about the stationary equilibrium: assume $r$ is a constant
    - Note that there's no population growth so we can set the number of members in each household as 1
## 2.2 模型求解：均衡条件
### 家庭部门的跨期优化（Euler Equation）
- Similar to the RCK model$$\frac{\dot{C}(t)}{C(t)} = r - \rho$$
### 最终产品生产者的优化 (派生需求)
- 最终产品部门处于完全竞争市场，通过最大化利润来决定对中间投入品 $L(i)$ 的需求。

    - Final output at time $t$:
    $$Y(t) = \left[ \int_0^{A(t)} L(i, t)^\phi di \right]^{1/\phi}$$
    - Total Cost at time $t$ is:$$\int_0^{A(t)} p(i, t)L(i, t)di$$
    - The final-goods producers maximize their profits at each time $t$ by choosing $L(i, t)$ for $i \in [0, A(t)]$
    - 这推导出中间投入品的反需求函数：$$L(i) = \frac {1}{p(i)}^{\frac{1}{\phi-1}} Y$$或者表述为 $p(i) = \frac{\partial Y}{\partial L(i)}$
    - 含义： 这建立了中间品价格 $p(i)$ 与需求量 $L(i)$ 之间的联系，是垄断者定价的基础。
- 成本最小化方案
    - $$\min_{\{L(i)\}_{i \in [0, A]}} \quad \int_0^A p(i)L(i)di$$
    -  $$s.t. \quad \left[ \int_0^A L(i)^\phi di \right]^{1/\phi} = 1$$
### R&D部门与中间品垄断者的优化（核心机制）
- 商根据最终产品部门的需求曲线设定价格，以最大化瞬时利润 π。结果是设定一个恒定的加价
    - $$\max_{\{p(i,t)\}} \pi(i, t) = p(i, t)L(i, t) - w(t)L(i, t) = [p(i, t) - w(t)] \left[ \frac{\lambda}{p(i, t)} \right]^{\frac{1}{1-\phi}}$$
    - FOC $$p(i) = \frac{w}{\phi}$$
    - 含义： 价格 p 是边际成本（工资 w）的倍数。因为 0<ϕ<1，所以价格始终高于边际成本。这是垄断利润的来源，也是回报研发投入的资金流
    - 生产商面临相同的需求弹性，他们会设定相同的垄断价格 $p(i,t) = p$。
    - $$L(i, t) = L_Y(t) / A(t)$$
    - As a result, we have$$Y(t) = A(t)^{\frac{1-\phi}{\phi}} L_Y(t)$$
- 研发部门的自由进入 (Free Entry Condition)
- 条件： 在均衡状态下，研发新想法的成本必须等于该想法未来垄断利润的净现值。
-厂商根据最终产品部门的需求曲线设定价格，以最大化瞬时利润 $\pi$。结果是设定一个恒定的加价
  
    - $$\frac{w(t)}{BA(t)} = \int_t^\infty e^{-r(\tau-t)}\pi(\tau)d\tau$$
    - 其中$$\pi(\tau) = p(i, \tau)L(i, \tau) - w(\tau)L(i, \tau)$$
    - 左边是生产一个新想法的边际成本（工资除以研发生产率）。The cost of producing a new idea at time t
    - 右边是拥有该专利带来的未来所有利润流的折现值，The present value of profits it can generate
### 市场出清条件（Market Clearing）
- 劳动力市场：$L_A + L_Y = \bar{L}$且根据对称性，生产部门劳动力均匀分布在所有中间品生产中
- 产品市场出清
    - 总产出等于总消费$C\bar{L} = Y$,且$Y = [\int_0^A L(i)^\phi di]^{1/\phi}$
- 模型最后总结
    - 将上述条件结合，我们可以解出模型的核心变量：
    - 对称性结果： 由于定价公式 $p = w/\phi$ 对所有 $i$ 相同，所有中间品的投入量也是相同的： $L(i) = L_Y/A(t)$。
    - 增长率关联： 结合生产函数和市场出清，产出和消费的增长率由 $A$ 的增长率决定： $\frac{\dot{Y}}{Y} = \frac{1-\phi}{\phi}g_A$。
    - 最终解 ($L_A$)： 联立自由进入条件和欧拉方程，最终解出均衡时的研发人员数量 $L_A$ 为常数：$$L_A = \frac{(1-\phi)\bar{L} - \phi\rho}{B}$$
## 2.3 一般均衡结果
    一般均衡被定义为一系列内生变量（如消费、产出、技术存量、价格、工资等）的时间序列，它们同时满足家庭效用最大化、厂商利润最大化、R&D部门自由进入以及市场出清条件
- 均衡时的研发人员数量
    $$L_A = \max \left\{ (1-\phi)\bar{L} - \frac{\phi\rho}{B}, 0 \right\} .$$
- the growth rate of output 
    $$\frac{\dot{Y}(t)}{Y(t)} = \max \left\{ \frac{(1-\phi)^2}{\phi} B\bar{L} - (1-\phi)\rho, 0 \right\} .$$
## 2.4 均衡参数与福利含义
### 均衡参数对增长的影响
- 主观贴现率 ：$\rho$: when individuals are less patient (that is, when $\rho$ is higher), fewer workers engage in R&D, and so growth is lower.
- 替代弹性 $\phi$: an increase in substitutability among inputs ($\phi$) also reduces growth.
-  R&D 生产率 $B$: an increase in productivity in the R&D sector ($B$) increases growth.
- 人口规模  $\bar{L}$: an increase in the size of the population ($\bar{L}$) raises long-run growth.
### 福利分析：市场均衡 vs. 社会最优
- Romer 模型的一个关键结论是：自由市场竞争达不到帕累托最优。
- 市场均衡 ($EQ$)： 私人企业根据利润最大化和自由进入条件决定 $L_A$。他们只关心自己能赚多少钱。
    - 市场均衡投入： $L_A^{EQ} = \frac{(1-\phi)\bar{L}-\phi\rho}{B}$
- 社会最优 ($OPT$)： 社会计划者根据代表性家庭的终身效用最大化来决定 $L_A$ 2 。计划者关心的是全社会的总福利。
    - 社会最优投入： $L_A^{OPT} = \bar{L} - \frac{\phi}{1-\phi} \frac{\rho}{B}$
### 低效的根源：三种外部性
- 消费者剩余效应:
    - 创新者虽然有专利，但只能按统一价格销售（垄断定价），无法实行完全价格歧视。因此，创新带来的社会总价值中，有一部分变成了最终产品生产商的“消费者剩余”。
    - 因为私人研发者拿不到这部分好处，他们的研发动力小于该技术对社会的真实贡献。
- R&D 效应
    - 每一个新想法的产生都增加了公共知识存量 A,更高的 A 会降低未来研发的成本.
    - 当前的研发者无法向“未来的研发者”收费，这种跨期溢出效应没有被市场定价。因此，私人部门忽视了自己对后人的贡献，导致投资不足。
- 商业窃取/创造效应
    - 新技术的引入可能会破坏旧技术的垄断地位，损害现有厂商的利润。
    - 私人研发者在决策时不会考虑这一对他人的损害。这理论上会导致过度研发，但在 Romer 模型的特定设定下，前两种正外部性占据主导地位，总体结果仍是研发不足。
# 3 human capital
## 模型设定与假设
### 生产函数： 
- 采用柯布-道格拉斯形式：$$Y(t) = K(t)^\alpha[A(t)H(t)]^{1-\alpha}$$
- 其中 $H(t)$ 代表不同技能水平工人的总贡献 。
- 人力资本构成：$$H(t) = L(t)G(E)$$
- 这里 $L(t)$ 是工人人数，$$\dot{L}(t) = nL(t), \quad L(0) \text{ given.}$$
- 而 $G(E)$ 是基于受教育年限 $E$ 的工人人均人力资本。通常假设 $G'(E) > 0$，例如 $G(E) = e^{\phi E}$ 5。
### Dynamics
- $$y(t) := \frac{Y(t)}{A(t)H(t)} = \frac{Y(t)}{A(t)L(t)G(E)}$$
- $$\quad k(t) := \frac{K(t)}{A(t)H(t)} = \frac{K(t)}{A(t)L(t)G(E)}$$
- $$\dot{k}(t) = sk(t)^\alpha - (n + g + \delta)k(t)$$
- the steady state is unique at$$k^* = \left[ \frac{s}{n + g + \delta} \right]^{1/(1-\alpha)}$$At the steady state, output will grow at the rate n + g.
### 关键权衡：(教育的)质量 vs. 数量
    人生总时长为 $T$，前$ E$ 年上学（不生产），后 $T−E$ 年工作
- 当受教育时间 E 增加时，发生两种截然相反的效果
    - 质量提升（正效应）： 工人技能 $G(E)$ 提高，导致每个工人的产出 $(Y/L)$ 增加
    - 数量减少（负效应）： 由于人们花更多时间上学，社会中实际工作的“工人占比” $(L(t)/N(t))$ 会下降
- the total population at t
$$\begin{aligned}
N(t) &= \int_{s=t-T}^{t} B(s)ds \\
&= \int_{\tau=0}^{T} B(t-\tau)d\tau \\
&= \int_{\tau=0}^{T} B(t)e^{-n\tau} d\tau \\
&= B(t) \int_{\tau=0}^{T} e^{-n\tau} d\tau \\
&= \frac{1 - e^{-nT}}{n} B(t)
\end{aligned}$$
- the number of workers at t 
$$\begin{aligned}
L(t) &= \int_{s=t-T}^{t-E} B(s)ds \\
&= \int_{\tau=E}^{T} B(t-\tau)d\tau \\
&= \int_{\tau=E}^{T} B(t)e^{-n\tau} d\tau \\
&= \frac{e^{-nE} - e^{-nT}}{n} B(t)
\end{aligned}$$
- Output per person
$$\frac{Y(t)}{N(t)} = \frac{L(t)}{N(t)} \frac{Y(t)}{L(t)} = y(t)A(t)G(E) \frac{e^{-nE} - e^{-nT}}{1 - e^{-nT}}$$
### “Golden Rule” Level of E
- $$E^* = T - \frac{1}{n} \ln \left( \frac{\phi}{\phi - n} \right)$$
- $E^∗$ can be equal to 0 under some condition on parameters ,but it cannot be equal to $T$
- Since $\frac{\partial E^*}{\partial T} = 1 > 0$. Increase in lifespan raises the golden rule level of education.
$$\begin{aligned}
\frac{\partial E^*}{\partial n} &= \frac{1}{n^2} \ln \left( \frac{\phi}{\phi - n} \right) - \frac{1}{n} \frac{1}{\phi - n} \\
&= \frac{1}{n^2} \left[ \ln \left( \frac{\phi}{\phi - n} \right) - \left( \frac{n}{\phi - n} \right) \right] \\
&= \frac{1}{n^2} [\ln(x) - (x - 1)] < 0
\end{aligned}$$
- Therefore a fall in $n$ raises $E^*$
### Endogenizing worker’s choice of E
- The equilibrium wage is equal to the marginal product of labor:$$w(t) = \frac{\partial Y}{\partial L} = (1 - \alpha) \left( \frac{K(t)}{A(t)H(t)} \right)^\alpha A(t)G(E)$$
- Suppose the economy is on the BGP at the very beginning,$$w(t) = (1 - \alpha)k^{*\alpha} A(0)e^{gt}e^{\phi E}$$
- So the present value of lifetime income of a representative worker is:
$$\begin{aligned}
Y &= \int_E^T e^{-\bar{r}t}w(t)dt \\
&= be^{\phi E} \int_E^T e^{-(\bar{r}-g)t} dt.
\end{aligned}$$
# 4 Real Business Cycle
## 基准 RBC 模型的设定
### Assumptions on Production
- Production:$$Y_t = K_t^\alpha(A_tL_t)^{1-\alpha}, \quad 0 < \alpha < 1$$
- Output is divided among consumption ($C$), investment ($I$), and government purchases ($G$).
- Capital depreciation rate is $\delta$.
- $$K_{t+1} = K_t + Y_t - C_t - G_t - \delta K_t$$
- Labor is measured by total work time.
### Assumptions on Household
$$U = \sum_{t=0}^{\infty} e^{-\rho t} u(c_t, 1 - l_t) \frac{N_t}{H}$$
- $\frac{N_t}{H}$: number of household members
- $1 - l_t$: leisure, $l_t = \frac{L_t}{N_t}$ (Assume time endowment per household member is normalized to 1, so leisure+work=1 )
- $c_t$: consumption per household member, $c_t = \frac{C_t}{N_t}$
- Instantaneous Utility Function: $$u_t = \ln(c_t) + b \ln(1 - l_t)$$
- Population grows exogenously at rate $n$: $\ln N_t = \bar{N} + nt$ so $N_t = e^{\bar{N}+nt}$
### 冲击的设定
技术冲击 $(A_t)$ 和 政府购买冲击 $(G_t)$ 遵循 AR(1)（一阶自回归）过程，包含持久性成分和随机白噪声.
- Technology shocks
$$  \ln(A_t) = \bar{A} + gt + \tilde{A}_t$$
$$  \tilde{A}_t = \rho_A \tilde{A}_{t-1} + \epsilon_{A,t}, \quad -1 < \rho_A < 1$$
- Government-purchases shocks
$$  \ln(G_t) = \bar{G} + (n + g)t + \tilde{G}_t$$
$$  \tilde{G}_t = \rho_G \tilde{G}_{t-1} + \epsilon_{G,t}, \quad -1 < \rho_G < 1$$
- Impulse Response Function
    - $$IRF_X(j) = \tilde{X}_{t+j}$$
    - 第 $t$ 期的冲击 $\epsilon_t$ 每增加 1 个单位，会引起 $j$ 期之后的变量 $X_{t+j}$ 变化多少？
    $$\begin{cases}
    \epsilon_\tau = \sigma & \text{如果 } \tau = t \text{ (冲击发生在当期)} \\
    \epsilon_\tau = 0 & \text{如果 } \tau \neq t \text{ (其他时期无冲击)}
    \end{cases}$$
## 优化问题与均衡
### Firm’s Optimization Problem
$$\max_{K_t, L_t} K_t^\alpha (A_t L_t)^{1-\alpha} - w_t L_t - r_t K_t - \delta K_t$$
- FOC (First Order Conditions)
$$  \begin{aligned}
  w_t &= (1-\alpha) K_t^\alpha A_t^{1-\alpha} L_t^{-\alpha} \\
  &= (1-\alpha) \frac{Y_t}{L_t}
  \end{aligned}$$

  $$  \begin{aligned}r_t &= \alpha K_t^{\alpha-1} (A_t L_t)^{1-\alpha} - \delta \\&= \alpha \frac{Y_t}{K_t} - \delta\end{aligned}$$
### Household’s Problem
$$\max_{\{c_t,l_t\}} E \left[ \sum_{t=0}^{\infty} e^{-\rho t} u(c_t, 1 - l_t)\frac{N_t}{H} \right]$$
$$s.t. \quad \frac{K_{t+1}}{H} = \frac{K_t}{H} + w_t l_t \frac{N_t}{H} + r_t \frac{K_t}{H} - \frac{G_t}{H} - c_t \frac{N_t}{H}$$
- Household’s Problem- One Period
$$  \max_{c,l} \ln(c) + b \ln(1 - l)$$
$$  s.t. \quad c = wl$$FOC:$$  \frac{1}{l} = \frac{b}{1 - l}$$
- Household’sProblem-TwoPeriods
$$  \max_{c_1,c_2,l_1,l_2} \ln(c_1) + b \ln(1 - l_1) + e^{-\rho}[\ln(c_2) + b \ln(1 - l_2)]$$
$$  s.t. \quad c_1 + \frac{1}{1+r}c_2 = w_1 l_1 + \frac{1}{1+r}w_2 l_2$$
FOC for $l_1$ and $l_2$:$$  \frac{1 - l_1}{1 - l_2} = \frac{1}{e^{-\rho}} \frac{w_2}{w_1(1 + r)}$$
### Informal Method
- 跨期优化
    - 今天的成本：$$\text{Cost} = e^{-\rho t} (N_t/H) (1/c_t) \Delta c$$
        - $1/c_t$: 这是边际效用，模型隐含假设了对数效用函数 $U(c) = \ln(c)$
    
        - $e^{-\rho t}$: 时间贴现因子
    - 明天的预期收益:$$\text{Benefit} = E_t [e^{-\rho(t+1)} (N_{t+1}/H) (1/c_{t+1}) e^{-n} (1+r_{t+1}) \Delta c]$$
        - 因为明天的利率 $r_{t+1}$ 和明天的消费情况 $c_{t+1}$ 在今天是不确定的（随机变量），所以要取期望。
        - $(1+r_{t+1})\Delta c$: 今天的 $\Delta c$ 存进银行，明天变成了这么多钱。这是资本回报。
        - $e^{-n}$: 人口增长调整。这通常用于处理人均变量。
    - 均衡条件
    $$\frac{1}{c_t} = e^{-\rho} E_t \left[ \frac{1}{c_{t+1}} (1+r_{t+1}) \right]$$
        - 左边 $\frac{1}{c_t}$：今天的边际效用。
        - 右边：明天的预期边际效用 $\times$ 投资回报 $\times$ 耐心程度（贴现因子）。
- 同期优化
    - 成本
    $$\text{Cost} = e^{-\rho t}(N_t/H) [b/(1 - l_t)] \Delta l$$
         $[b/(1 - l_t)]$: 这是 闲暇的边际效用
         隐含假设： 从这里可以看出，该模型使用的效用函数包含类似于 $b \ln(1-l_t)$ 的项。因为对 $l_t$ 求导得到 $\frac{b}{1-l_t}$。
    - 收益
    $$\text{Benefit} = e^{-\rho t}(N_t/H) (1/c_t) w_t \Delta l$$
    - 均衡条件
    $$\frac{c_t}{1 - l_t} = \frac{w_t}{b}$$
    $$b \frac{c_t}{1-l_t} = w_t \quad \Rightarrow \quad \frac{b/(1-l_t)}{1/c_t} = w_t$$

    - 分子 $b/(1-l_t)$ 是闲暇的边际效用 ($MU_{leisure}$)。
    - 分母 $1/c_t$ 是消费的边际效用 ($MU_{consumption}$)。
    - 含义： 边际替代率 (MRS) 等于实际工资 ($w_t$)。
     $$ MRS_{lc} = w_t $$
### A Special Case（暂无）
# 5  动态规划与贝尔曼方程
## 动态规划（Dynamic Programming, DP）
- 核心思想是将一个复杂的无限期问题分解为一系列简单的“两期”子问题（当前 vs 未来）。
    - 动态规划将随时间变化的优化问题视为**“分阶段优化（Optimization in stages）”**。我们需要在“当前阶段获得最佳结果”与“该决策对未来阶段的影响”之间进行权衡
    为了实现这一点，必须定义两类关键变量：
        - 状态变量 (State Variable, $x_t$或 $k_t$)： 在特定时间点 t，决策者所面临的既定状况（如当前的资本存量）。它是决策的出发点，被视为给定的.
        - 控制变量 (Control Variable, $u_t或 c_t,k_t+1$)： 决策者在当前时间点可以选择的变量。通常，选择当前的控制变量（如消费或投资）决定了下一期的状态变量（如明天的资本存量）
- 价值函数 (Value Function)
    - 价值函数 $V(K_t,A_t)$ 定义为：给定当前的状态变量（如资本存量 $K_t$和技术水平 $A_t$），从现在开始一直到未来，家庭能够获得的最大化效用现值。

    At time $t$, given $k_t$, we can write$$V(k_t) = \max_{\{k_{t+1+i}\}_{i=0}^\infty} \sum_{i=0}^{\infty} \beta^i u((1+r)k_{t+i} - k_{t+1+i})$$
    At time $t+1$, given $k_{t+1}$, we can write$$V(k_{t+1}) = \max_{\{k_{t+1+i}\}_{i=1}^\infty} \sum_{i=0}^{\infty} \beta^i u((1+r)k_{t+1+i} - k_{t+2+i})$$
- 最优性原理(Principle of Optimality)
    - 最优性原理指出，无论初始状态和第一步决策是什么，余下的决策相对于由第一步决策所产生的状态而言，必须构成一个最优策略。
### Bellman Equation
$$\begin{aligned}
V(k_t) &= \max_{\{k_{t+1+i}\}_{i=0}^\infty} \sum_{i=0}^{\infty} \beta^i u((1+r)k_{t+i} - k_{t+1+i}) \\
&= \max_{k_{t+1}} \{ u((1+r)k_t - k_{t+1}) \\
&\quad + \max_{\{k_{t+1+i}\}_{i=1}^\infty} \sum_{i=0}^{\infty} \beta^{i+1} u((1+r)k_{t+1+i} - k_{t+2+i}) \} \\
&= \max_{k_{t+1}} \{ u((1+r)k_t - k_{t+1}) + \beta V(k_{t+1}) \}
\end{aligned}$$
- 贝尔曼方程将无限期的求和简化为“当前回报”与“折现后的未来价值”之和

- 通过分析贝尔曼方程来求解模型，这一过程主要依赖于两个关键的数学条件
- 一阶条件 (First Order Condition, FOC)：
    - 对贝尔曼方程右侧（RHS）的控制变量求导，并令其为 0。它权衡了“当前改变控制变量带来的回报变化”与“未来价值的变化”。
    $$u'((1+r)k_t - k_{t+1}) = \beta V'(k_{t+1}).$$
    or$$u'(c_t) = \beta V'(k_{t+1}).$$
    - But we still don't know what $V'(k_{t+1})$ is.
- 包络条件 (Envelope Condition)
    - 对贝尔曼方程左侧 $V(x_t)$ 关于状态变量 $x_t$求导。
    - 虽然最优控制变量 $u^∗$也是状态变量的函数，但在对 $V(x_t)$ 求导时，可以忽略控制变量的间接影响（因为根据 FOC，该点的一阶导数已经为 0）
    - $$V'(k_{t+1}) = u'((1+r)k_{t+1} - k_{t+2})(1+r)$$
    - $$V'(k_{t+1}) = u'(c_{t+1})(1+r)$$
### Euler Equation
- Combine the first order condition and the envelope condition, we can get the Euler equation:$$\frac{u'(c_t)}{u'(c_{t+1})} = \beta(1 + r)$$
- If we assume ln utility:$$\frac{c_{t+1}}{c_t} = \beta(1 + r)$$
### Optimal Policy Function
- Apply the budget constraint $k_t = \frac{1}{1+r}(k_{t+1} + c_t)$ recursively, we can show $$(1+r)k_t = \sum_{j=0}^{\infty} \left( \frac{1}{1+r} \right)^j c_{t+j}.$$
- Euler equation implies $c_{t+j} = [\beta(1+r)]^j c_t$. Combine above results, we can show the optimal policy function is:$$c_t^* = (1-\beta)(1+r)k_t^*$$ $$or \quad k_{t+1}^* = \beta(1+r)k_t^*$$
- That is, optimal consumption at each time is proportional to the state variable $k_t$.
### 一般化问题
- 一般化问题的设定:任何动态优化问题都可以被抽象为以下标准形式：
    $$\max \quad E \left\{ \sum_{t=0}^{\infty} \beta^t f(x_t, u_t) \right\}$$
    $$s.t \quad x_{t+1} = G(x_t, u_t),$$
    $$x_0 \text{ is given.}$$
    $x_t$ is the state variable and $u_t$ is the control variable at time $t$.
- 通用求解指南：四步法:核心在于推导欧拉方程
    - 步骤 1：建立贝尔曼方程:将无限期问题转化为“两期”递归问题。当前价值等于“当期回报”加上“预期的折现未来价值”
    $$  \begin{aligned}
  V(x_t) &= \max_u \{ f(x_t, u_t) + E_t \beta V(x_{t+1}) \} \\
  &= \max_u \{ f(x_t, u_t) + E_t \beta V(G(x_t, u_t)) \}
  \end{aligned}$$
  - 求解一阶条件 (FOC):对贝尔曼方程右侧的控制变量 $u_t$求导并令其为 0。这是为了找到当前的最优决策： $$f_2(x, u) + E_t \beta G_2(x, u) V'(G(x, u)) = 0$$
  - 求解包络条件 (Envelope Condition):对贝尔曼方程左侧的状态变量 $x_t$求导。
   $$V'(x) = f_1(x, u) + E_t \beta G_1(x, u) V'(G(x, u))$$
- 推导欧拉方程与策略函数
    - 如果 $G_1 = 0$,那么$V'(k_t) = \frac{\partial u(c_t)}{\partial k_t} = u'(c_t) \cdot (1+r)$
    - 复杂情况 ($G_1 \neq 0$)
        - 有时我们可以通过合理定义控制变量和状态变量，使得 $G_1 = 0$。
        待定系数法,猜测价值函数的参数形式:（例如：猜它是线性的、对数的或二次的），然后验证它。
        迭代法 (Method of Iterations):猜测一个初始的价值函数作为起点，利用迭代（通常由计算机完成）直到价值函数收敛。
### 充分性验证与横截条件
我们如何确保从贝尔曼方程解出的函数 $V(\cdot)$ 确实给出了原始问题的最优目标函数值？
- 充分性验证
    - $V(x_t) \ge f(x_t, u_t) + \beta E_t V(x_{t+1})$ 
    - 两边乘以 $\beta^t$：$\beta^t V(x_t) - \beta^{t+1} E_t V(x_{t+1}) \ge \beta^t f(x_t, u_t)$
    - 对 $t=0$ 时刻取期望，并对 $t$ 进行求和（累加）：$$V(x_0) - \lim_{T \to \infty} \beta^T E_0 V(x_T) \ge E_0 \{ \sum_{t=0}^{\infty} \beta^t f(x_t, u_t) \}$$
- 横截条件
    - 一个充分条件是 $\lim_{T \to \infty} \beta^T E_0 V(x_T) = 0$。
    - 在满足某些正则性假设的前提下：$\lim_{T \to \infty} \beta^T E_0 V'(x_T)x_T = 0$。
### Application to the RBC Model
- 核心技巧：变量选择的转换
    - 控制变量 (Control Variable) 的选择： 通常我们认为消费 $c_t$是控制变量，但资料建议直接将下一期资本 $K_{t+1}$视为控制变量
    $c_t = w_t l_t - \frac{K_{t+1} - (1+r_t)K_t + G_t}{N_t}$
    - 状态变量 (State Variable)： 保持为当期资本 $K_t$
    - 状态转移函数（Transition Function）变得极其简单$K_{t+1} = G(K_t, K_{t+1}) = K_{t+1}$
    - As a result, $G_1 \equiv 0$ and $G_2 \equiv 1$.
- 建立随机贝尔曼方程
    - 我们建立 RBC 模型的贝尔曼方程。这里需要同时决定两个控制变量：下一期资本 $K_{t+1}$和 劳动供给 $l_t$。
    $$V(K_t) = \max \left\{ u \left( w_t l_t - \frac{K_{t+1} - (1 + r_t)K_t + G_t}{N_t}, 1 - l_t \right) \frac{N_t}{H} + e^{-\rho} E_t[V(K_{t+1})] \right\}$$
- 求解一阶条件 (FOC)
    - with respect to $l_t$:$$u_1(c_t, 1 - l_t)w_t = u_2(c_t, 1 - l_t)$$
    - with respect to $K_{t+1}$:$$\frac{u_1(c_t, 1 - l_t)}{H} = e^{-\rho} E_t[V'(K_{t+1})]$$
- 利用包络条件 (Envelope Condition)
    - 由于我们巧妙地设定了$G_1 \equiv 0$，包络定理的应用变得非常直接。我们对状态变量$K_t$求导：
    - 当前时刻： 
    - $$V'(K_t) = u_1(c_t, 1 - l_t)\frac{1 + r_t}{H}$$
    - 下一时刻（迭代形式）
    - $$V'(K_{t+1}) = u_1(c_{t+1}, 1 - l_{t+1})\frac{1 + r_{t+1}}{H}$$
- 推导欧拉方程 (Euler Equation)
    - FOC with respect to $l_t$
    $$  \frac{w_t}{c_t} = \frac{b}{1 - l_t}$$
    - FOC with respect to $K_{t+1}$ with Envelope Theorem
    $$  \frac{1}{c_t H} = e^{-\rho} E_t \left[ u_1(c_{t+1}, 1 - l_{t+1}) \frac{1 + r_{t+1}}{H} \right]$$
    $$  \iff \quad \frac{1}{c_t} = e^{-\rho} E_t \left[ \frac{1}{c_{t+1}} (1 + r_{t+1}) \right]$$
- 求解难点与后续方法
    - 虽然我们推导出了欧拉方程，但获得解析解（Analytical Solution）依然困难
    - 解决方法：
        - 对数线性化 (Log-linearization)： 通过线性近似来简化期望项（这是 RBC 分析的常用手段）。
        - 猜想与验证 (Guess-and-verify)： 对于特定形式的效用函数（如对数效用），可以猜想策略函数的形式,然后验证其系数