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

# Разложение на корневые подпространтва

$\oplus$ - прямая сумма

**Лемма 1**: $[\mathcal{L} = \text{Ker} \mathcal{A} \oplus \text{Im} \mathcal{A}] \Leftrightarrow [\text{Ker} \mathcal{A} = \text{Ker} \mathcal{A}^2]$

$\square$

По формуле Грассмана $\dim(\text{Ker} \mathcal{A} + \text{Im} \mathcal{A}) = \dim\text{Ker} \mathcal{A} + \dim\text{Im} \mathcal{A} - \dim(\text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A})$

Из курса линейной алгебры известно $\dim\text{Ker} \mathcal{A} + \dim\text{Im} \mathcal{A} = \dim\mathcal{L}$

$\blacksquare$

**Лемма 2**: $\mathcal{V}_\lambda$ - подпространство инвариантное относительно $\mathcal{A}$

$\square$

Выберем любой $x \in \mathcal{V}_\lambda$

Очевидно $\mathcal{A}_\lambda x \in \mathcal{V}_\lambda$, $\lambda x \in \mathcal{V}_\lambda$

Окончательно $\mathcal{A} x = \mathcal{A}_\lambda x + \lambda x \in \mathcal{V}_\lambda$

$\blacksquare$


**Теорема 4**: $[\lambda_1, ..., \lambda_s$ - собственные значения $\mathcal{A}] \Rightarrow [\mathcal{L} = \bigoplus\limits_{i=1}^s \mathcal{V}_{\lambda_i}]$

$\square$

Обозначим $\lambda = \lambda_1$

В силу **теоремы 3** $\forall p \ge h_\lambda \mapsto \mathcal{V}_\lambda = \text{Ker} \mathcal{A}_\lambda^p \Rightarrow \mathcal{V}_\lambda = \text{Ker} \mathcal{A}_\lambda^{h_\lambda} = \text{Ker} \mathcal{A}_\lambda^{2 h_\lambda}$

По **лемме 1** получаем $\mathcal{L} = \mathcal{V}_{\lambda_1} \oplus \mathcal{W}_1$, $\mathcal{W}_1 = \text{Im} \mathcal{A}_\lambda^{h_\lambda}$

$\lambda_2, ..., \lambda_s$ - собственные значения $\mathcal{A}|_{\mathcal{W}_1}$

Рассуждая аналогично для $\lambda_2, ..., \lambda_s$, получаем:

$\mathcal{L} = \mathcal{V}_{\lambda_1} \oplus ... \oplus \mathcal{V}_{\lambda_s} \oplus \mathcal{W}$

Здесь $\mathcal{W}$ не может иметь собственных векторов, так как они все лежат в $\mathcal{V}_{\lambda_1}$ ..., $\mathcal{V}_{\lambda_s}$, но поле $\mathbb{C}$ алгебралически замкнуто $\Rightarrow \dim\mathcal{W} = 0$, иначе характеристическое уравнение для $\mathcal{A}|_\mathcal{W}$ имеет корень и в $\mathcal{W}$ есть собственные векторы

$\blacksquare$

Замечание: Если поле не является алгебралически замкнутым(например $\mathbb{R}$), то справедливо представление $\mathcal{L} = \left( \bigoplus\limits_{i=1}^s \mathcal{V}_{\lambda_i} \right) \oplus \mathcal{W}$

**Теорема 5**: Существует базис в котором $A = \text{diag}(A|_{\mathcal{V}_{\lambda_1}}, ..., A|_{\mathcal{V}_{\lambda_s}})$

$\square$

Выберем в $\mathcal{V}_{\lambda_k}$ базис $e^{(k)}_{1}, ..., e^{(k)}_{n_{\lambda_k}}, k = \overline{1,s}$

В силу **теоремы 4** объединение базисов $e^{(1)}_{1}, ..., e^{(1)}_{n_{\lambda_1}}, ..., e^{(s)}_{1}, ..., e^{(s)}_{n_{\lambda_s}}$ - базис в $\mathcal{L}$

Но из **леммы 2** следует, что в этом базисе матрица преобразования имеет необходимый вид

$\blacksquare$