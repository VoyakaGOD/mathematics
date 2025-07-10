# Введение

Будем рассматривать линейное пространство $\mathcal{L}$ над полем $\mathbb{C}$.

Конечной размерности $\dim\mathcal{L} = n$

И линейное преобразование $\mathcal{A}: \mathcal{L} \rightarrow \mathcal{L}$ с матрицей $A \in \mathbb{C}^{n \times n }$

$\mathcal{E}$ - тождественное преобразование, $E \in \mathbb{C}^{n \times n}$ - его матрица

**Определение 0**: $\N_0 = \N \cup \{0\}$

# Собственные и коренвые векторы

Фиксируем $\lambda \in \mathbb{C}$ и расммотрим оператор $\mathcal{A}_\lambda = \mathcal{A} - \lambda\mathcal{E}$ 
с матрицей $A_\lambda = A - \lambda E$

**Определение 1**: $x \in \mathcal{L}: x \neq 0, \mathcal{A}x = \lambda x$ называется собственным вектором с собственным значением $\lambda$

**Определение 2**: $x \in \mathcal{L}: \exists p \in \N_0 \;\; \mathcal{A}_\lambda^p x = 0$ называется коренвым вектором

**Определение 3**: Минимальное $p$ из **определения 2** будем называть высотой вектора $h_\lambda(x) = p_{min}$

Следствие 1: $\forall \lambda \in \mathbb{C} \mapsto h_\lambda(0) = 0$

Следствие 2: Собственные векторы и только они имеют высоту $1$

# Корневые подпространства

**Определение 4**: $\mathcal{L}_\lambda = \{ x \in \mathcal{L} | \mathcal{A}x = \lambda x \}$ - собственное подпространтсво $\mathcal{L}$ c собственным значением $\lambda$

**Определение 5**: $\mathcal{V}_\lambda = \{ x \in \mathcal{L} | \mathcal{A}_\lambda^p x = 0, p \in \N_0 \}$ - корневое подпространтсво $\mathcal{L}$

Несложно проверить, что $\mathcal{L}_\lambda$, $\mathcal{V}_\lambda$ - линейные подпространства $\mathcal{L}$

**Теорема 1**: $[\mathcal{V}_\lambda \neq \{0\}] \Leftrightarrow [\mathcal{L}_\lambda \neq \{0\}]$

$\square$

Очевидно $\mathcal{L}_\lambda \subset \mathcal{V}_\lambda$, то есть $[\mathcal{L}_\lambda \neq \{0\}] \Rightarrow [\mathcal{V}_\lambda \neq \{0\}]$

Обратно пусть $\mathcal{V}_\lambda \neq \{0\}$, тогда $\exists p \in \N, x_p \in \mathcal{L}: x \neq 0, \mathcal{A}_\lambda x \neq 0, ..., \mathcal{A}_\lambda^{p-1} x_p \neq 0, \mathcal{A}_\lambda^p x_p = 0$

Рассмотрим $x = \mathcal{A}_\lambda^{p-1} x_p \neq 0$, полагая $\mathcal{A}_\lambda^0 = \mathcal{E}$

Тогда $\mathcal{A}_\lambda x = 0 \Rightarrow \mathcal{L}_\lambda \neq \{0\}$

$\blacksquare$

Поэтому будем называть $\mathcal{V}_\lambda$ корневым подпространтсвом $\mathcal{L}$ c собственным значением $\lambda$

Размерность $\dim\mathcal{L} = n$ конечна $\Rightarrow \dim\mathcal{V}_\lambda = n_\lambda < n$ тоже конечна

**Теорема 2**: $[x \in \mathcal{L}: h_\lambda(x) = p > 1] \Rightarrow [x_0 = x, x_1 = \mathcal{A}_\lambda x, ..., x_{p-1} = \mathcal{A}_\lambda^{p-1} x$ - линейно независимы$]$

$\square$

Рассмотрим произвольную линейную комбинацию $\alpha_0 x_0 + ... + \alpha_{p-1} x_{p-1} = 0$

Действуем оператором $\mathcal{A}_\lambda$ на это равенство $(p-1)$-раз:

$\alpha_0 x_1 + ... + \alpha_{p-2} x_{p-1} = 0$

...

$\alpha_0 x_{p-2} + \alpha_1 x_{p-1} = 0$

$\alpha_0 x_{p-1} = 0$

Но $x_k \neq 0 \Rightarrow a_k = 0, k = \overline{0, p-1}$

$\blacksquare$

Следствие 1: $\forall x \in \mathcal{V}_\lambda \mapsto h_\lambda(x) \le n_\lambda$

**Определение 6**: $h(\mathcal{V}_\lambda) = \max\limits_{x \in \mathcal{V}_\lambda} h_\lambda(x)$ - высота корневого подпространства

Следствие 2: $h_\lambda = h(\mathcal{V}_\lambda) \le \dim\mathcal{V}_\lambda = n_\lambda$

**Теорема 3**: $\mathcal{V}_\lambda = \text{Ker} \mathcal{A}_\lambda^{h_\lambda}$

$\square$

По определению $\mathcal{V}_\lambda$ выполняется $\text{Ker} \mathcal{A}_\lambda^{h_\lambda} \subset \mathcal{V}_\lambda$

Обратно в силу **определения 6** верно $\forall x \in \mathcal{V}_\lambda \mapsto h_\lambda(x) \le h_\lambda \Rightarrow \mathcal{A}_\lambda^{h_\lambda} x = 0 \Rightarrow \mathcal{V}_\lambda \subset \text{Ker} \mathcal{A}_\lambda^{h_\lambda}$

$\blacksquare$
