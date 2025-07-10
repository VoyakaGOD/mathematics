# Введение

Будем рассматривать линейное пространство $\mathcal{L}$ над полем $\mathbb{C}$.

Конечной размерности $\dim\mathcal{L} = n$

И линейное преобразование $\mathcal{A}: \mathcal{L} \rightarrow \mathcal{L}$ с матрицей $A \in \mathbb{C}^{n \times n }$

$\mathcal{E}$ - тождественное преобразование, $E \in \mathbb{C}^{n \times n}$ - его матрица

**Определение 0**: $\N_0 = \N \cup \{0\}$

# Собственные и коренвые векторы

Фиксируем $\lambda \in \mathbb{C}$ и расммотрим оператор $\mathcal{A}_\lambda = \mathcal{A} - \lambda\mathcal{E}$ 
с матрицей $A_\lambda = A - \lambda E$

**Определение 1**: $x \in \mathcal{L}: x \neq 0, \mathcal{A}x = \lambda x$ называется собственным вектором

**Определение 2**: $x \in \mathcal{L}: \exists p \in \N_0 \;\; \mathcal{A}_\lambda^p x = 0$ называется коренвым вектором

**Определение 3**: Минимальное $p$ из **определения 2** будем называть высотой вектора $h_\lambda(x) = p_{min}$

Следствие 1: $\forall \lambda \in \mathbb{C} \mapsto h_\lambda(0) = 0$

Следствие 2: Собственные векторы и только они имеют высоту $1$
