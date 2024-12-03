<!-- vscode-markdown-toc -->
# Landau-Ginzburg Model Under Hard Constraint

1. [Soliton solution of Landau-Ginzburg model under hard constraint](#SolitonsolutionofLandau-Ginzburgmodelunderhardconstraint)
2. [Periodic solution of Landau-Ginzburg model under hard constraint](#PeriodicsolutionofLandau-Ginzburgmodelunderhardconstraint)

<!-- vscode-markdown-toc-config
	numbering=true
	autoSave=true
	/vscode-markdown-toc-config -->
<!-- /vscode-markdown-toc -->
##  1. <a name='SolitonsolutionofLandau-Ginzburgmodelunderhardconstraint'></a>Soliton solution of Landau-Ginzburg model under hard constraint

考慮硬限制條件下的孤子解（例如 $\phi \in [-1/2, 1/2]$），我們從一維的 Landau-Ginzburg 泛函出發，並根據邊界條件和硬限制進行計算。

假設場泛函為：

$\mathcal{H}[\phi] = \int dx \left[ \frac{1}{2} \left( \frac{d\phi}{dx} \right)^2 + V(\phi) \right],$

其中勢能 $V(\phi)$ 包含二次項和四次項：

$V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4 - h \phi.$

硬限制條件為：
$\phi(x) \in [-1/2, 1/2], \quad \forall x.$

對應的歐拉-拉格朗日方程為：
$\frac{d^2 \phi}{dx^2} = \frac{\partial V(\phi)}{\partial \phi}.$

在硬限制條件下，若 $\phi(x)$ 超出 $[-1/2, 1/2]$，則視為無效解。

孤子解的特徵：
- 系統具有兩個穩態（或準穩態），例如 $\phi = -1/2$ 和 $\phi = 1/2$，孤子連接這兩個態；
- 孤子解通常在無窮遠處滿足固定邊界條件，例如：
  $\phi(x \to -\infty) = -1/2, \quad \phi(x \to +\infty) = 1/2.$


方程：
$\frac{d^2 \phi}{dx^2} = \frac{\partial V(\phi)}{\partial \phi}.$

乘上 $\frac{d\phi}{dx}$ 並積分，可以得到能量守恆形式：

$\frac{1}{2} \left( \frac{d\phi}{dx} \right)^2 = V(\phi) + C,$

其中 $C$ 是積分常數。

選擇孤子邊界條件：

$\phi(x \to -\infty) = -1/2, \quad \phi(x \to +\infty) = 1/2,$

勢能在這兩個點相等，通常設定 $V(-1/2) = V(1/2) = 0$。這樣積分常數 $C = 0$。

因此：
$\frac{1}{2} \left( \frac{d\phi}{dx} \right)^2 = V(\phi).$

勢能在邊界的行為：
在硬限制條件下，$\phi(x)$ 的運動被約束在 $[-1/2, 1/2]$。勢能 $V(\phi)$ 通常設計為對稱雙井結構。例如：

$V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4.$

將硬限制邊界加入計算，要求：
$\phi(x) \to -1/2$ 和 $\phi(x) \to 1/2$ 處的運動滿足邊界條件，不進入邊界之外。

對於對稱勢能 $V(\phi)$，孤子解可以通過分離變數求解：

$\frac{d\phi}{\sqrt{2V(\phi)}} = dx.$

例如，對 $V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4$，勢能在硬限制邊界 $\phi = \pm 1/2$ 處被剪裁為有限值，計算過程如下：


$\int \frac{d\phi}{\sqrt{r\phi^2 + \frac{u}{2} \phi^4}} = \int dx.$

設定 $\phi = \tanh(kx)$ 作為試探解（孤子解通常具有這種形式），並代入方程，求解 $k$ 與參數 $r, u$ 的關係。


將勢能寫為標準形式：

$V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4.$

積分公式為：

$\frac{d\phi}{dx} = \sqrt{2 \left[ V(\phi_{\infty}) - V(\phi) \right]},$

其中 $V(\phi_{\infty}) = 0$（在邊界 $\phi = \pm 1/2$ 時勢能歸零）。因此，積分式成為：

$\int \frac{d\phi}{\sqrt{r \phi^2 + \frac{u}{2} \phi^4}} = x + \text{C}.$


將分母中的高次項提取出來，重新表達為：

$\int \frac{d\phi}{\sqrt{\phi^2 \left( r + \frac{u}{2} \phi^2 \right)}}.$

進一步進行變數代換。


設 $\phi = A \sin\theta$，其中 $A^2 = -\frac{2r}{u}$（這使得分母簡化），則：

$d\phi = A \cos\theta \, d\theta, \quad \phi^2 = A^2 \sin^2\theta.$

代入後，分母變為：

$\sqrt{\phi^2 \left( r + \frac{u}{2} \phi^2 \right)} = \sqrt{A^2 \sin^2\theta \left( r + \frac{u}{2} A^2 \sin^2\theta \right)}.$

由於 $A^2 = -\frac{2r}{u}$，可以簡化為：

$\sqrt{r \phi^2 + \frac{u}{2} \phi^4} = A |\sin\theta| \sqrt{r \left( 1 + \sin^2\theta \right)}.$

然後積分變為：

$\int \frac{A \cos\theta \, d\theta}{A |\sin\theta| \sqrt{r \left( 1 + \sin^2\theta \right)}}$

約簡後，積分形式為：

$\int \frac{\cos\theta}{|\sin\theta| \sqrt{1 + \sin^2\theta}} \, d\theta.$


設 $\sin\theta = t$，則 $\cos\theta \, d\theta = dt$，積分化為：

$\int \frac{dt}{|t| \sqrt{1 + t^2}}.$


由於 $t = \sin\theta$，這要求 $|t| \leq 1$。分母的 $\sqrt{1 + t^2}$ 可以直接寫成標準的反雙曲正切函數。

孤子解的形式為：

$\phi(x) = \pm \frac{1}{2} \tanh\left( k x \right),$

其中 $k = \sqrt{-2r/u}$ 是孤子解的特徵長度尺度。孤子在邊界 $\phi = \pm 1/2$ 處的行為符合硬限制；它的核心區域（磁化翻轉）具有寬度 $\propto 1/k$。

##  2. <a name='PeriodicsolutionofLandau-Ginzburgmodelunderhardconstraint'></a>Periodic solution of Landau-Ginzburg model under hard constraint

$\mathcal{H}[\phi] = \int dx [\frac{1}{2}( \frac{d\phi}{dx})^2 + V(\phi)]$

其中：

$V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4$

硬限制條件為：
$\phi(x) \in [-1/2, 1/2]$

歐拉-拉格朗日方程為：
$\frac{d^2\phi}{dx^2} = \frac{\partial V(\phi)}{\partial \phi} = r\phi + u\phi^3$

其中 $\phi(x)$ 在空間中呈現週期性變化。


類似粒子在有效勢 $V(\phi)$ 中的運動。通過能量守恆關係：
$\frac{1}{2} (\frac{d\phi}{dx})^2 + V(\phi) = E$

其中 $E$ 是有效能量。

令：
$\frac{d\phi}{dx} = \pm \sqrt{2(E - V(\phi))}$

目標是尋找週期解，即 $\phi(x)$ 在某區間 $[-\phi_0, \phi_0]$ 內來回振盪，並滿足硬限制 $[-1/2, 1/2]$。


$x = \int \frac{d\phi}{\sqrt{2(E - V(\phi))}}$

解的週期 $T$ 為：
$T = 2 \int_{-\phi_0}^{\phi_0} \frac{d\phi}{\sqrt{2(E - V(\phi))}}$

此處 $\phi_0$ 是振幅，滿足 $E = V(\phi_0)$。根據硬限制條件，我們需要 $\phi_0 \leq 1/2$。


對於 $V(\phi) = \frac{r}{2} \phi^2 + \frac{u}{4} \phi^4$，週期積分成為：
$T = 2 \int_{-\phi_0}^{\phi_0} \frac{d\phi}{\sqrt{2 \left( E - \frac{r}{2} \phi^2 - \frac{u}{4} \phi^4 \right)}}$

透過對稱性，積分簡化為：
$T = 4 \int_{0}^{\phi_0} \frac{d\phi}{\sqrt{2 \left( E - \frac{r}{2} \phi^2 - \frac{u}{4} \phi^4 \right)}}$

設 $E = \frac{r}{2} \phi_0^2 + \frac{u}{4} \phi_0^4$，分母可以重新表達為：
$\sqrt{2(E - V(\phi))} = \sqrt{r (\phi_0^2 - \phi^2) + \frac{u}{2} (\phi_0^4 - \phi^4)}$

將分母因式分解，變數代換可進一步處理。

令 $\phi = \phi_0 \sin\theta$，則：
$d\phi = \phi_0 \cos\theta \, d\theta, \quad \phi^2 = \phi_0^2 \sin^2\theta$


分母變為：
$\sqrt{\phi_0^2 (1 - \sin^2\theta) \left( r + \frac{u}{2} \phi_0^2 (1 + \sin^2\theta) \right)}$

積分變為：
$T = 4 \int_{0}^{\pi/2} \frac{\phi_0 \cos\theta \, d\theta}{\sqrt{\phi_0^2 \cos^2\theta \left( r + \frac{u}{2} \phi_0^2 (1 + \sin^2\theta) \right)}}$

約掉公因式後，積分化為：
$T = \frac{4}{\sqrt{r + \frac{u}{2} \phi_0^2}} \int_{0}^{\pi/2} \frac{d\theta}{\sqrt{1 - k^2 \sin^2\theta}}$

其中：
$k^2 = \frac{\frac{u}{2} \phi_0^2}{r + \frac{u}{2} \phi_0^2}$

這是標準的**第一類完全橢圓積分**：
$T = \frac{4}{\sqrt{r + \frac{u}{2} \phi_0^2}} K(k)$

其中：
$K(k) = \int_{0}^{\pi/2} \frac{d\theta}{\sqrt{1 - k^2 \sin^2\theta}}$

振幅 $\phi_0$ 和參數 $r, u$ 決定了橢圓積分的模數 $k$；週期 $T$ 為橢圓積分 $K(k)$ 的函數。

數值上，$\phi(x)$ 的解通常用**雅可比橢圓函數**表達為：
$\phi(x) = \phi_0 \, \text{sn}\left( \frac{2K(k)}{T} x, k \right)$

其中 $\text{sn}(x, k)$ 是第一類雅可比橢圓函數。

