# Введение

Будем рассматривать линейное пространство $\mathcal{L}$ над полем $\mathbb{C}$.

Конечной размерности $\dim\mathcal{L} = n$

И линейное преобразование $\mathcal{A}: \mathcal{L} \rightarrow \mathcal{L}$ с матрицей $A \in \mathbb{C}^{n \times n }$

$\mathcal{E}$ - тождественное преобразование, $E \in \mathbb{C}^{n \times n}$ - его матрица

$\Theta$ - нулевое преобразование

**Определение 0**: $\N_0 = \N \cup \{0\}$

$\mathcal{A}|_\mathcal{U}: \mathcal{U} \rightarrow \mathcal{U}$ - ограничение $\mathcal{A}$ на инвариантное линейное подпространство $\mathcal{U}$ с матрицей $A|_\mathcal{U}$

$\text{diag}(A_1, ..., A_s)$ - блочно-диагональная матрица

$\langle e_1, ..., e_s \rangle = \{x = \sum\limits_{i=1}^s \alpha_i e_i | \alpha_1, ..., \alpha_s \in \mathbb{C} \}$ - линейная оболочка векторов $e_1, ..., e_s$

$|A|$ - определитель матрицы $A$

# Собственные и коренвые векторы

Фиксируем $\lambda \in \mathbb{C}$ и расммотрим оператор $\mathcal{A}_\lambda = \mathcal{A} - \lambda\mathcal{E}$ 
с матрицей $A_\lambda = A - \lambda E$

**Определение 1.1**: $x \in \mathcal{L}: x \neq 0, \mathcal{A}x = \lambda x$ называется собственным вектором с собственным значением $\lambda$

**Определение 1.2**: Многочлен ${\Large\chi}(\lambda) = |A - \lambda E|$ называется характеристическим для матрицы $A$

$|S^{-1}AS - \lambda E| = |S^{-1}||A - \lambda E||S| = |A - \lambda E| \Rightarrow$ он не меняется при смене базиса, поэтому его также называют характеристическим многочленом преобразования $\mathcal{A}$ и обозначают ${\Large\chi}_{\mathcal{A}}(\lambda)$

$\lambda$ - собственное значение оператора $\mathcal{A} \Leftrightarrow \text{Ker}(\mathcal{A} - \lambda \mathcal{E}) \neq \{0\} \Leftrightarrow {\Large\chi}_{\mathcal{A}}(\lambda) = 0$

**Определение 1.3**: ${\Large\chi}_{\mathcal{A}}(\lambda) = 0$ называют характеристическим уравнением

**Определение 2**: $x \in \mathcal{L}: \exists p \in \N_0 \;\; \mathcal{A}_\lambda^p x = 0$ называется корневым вектором

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

Два эквививалентных определения прямой суммы $\mathcal{L} = \bigoplus\limits_{i=1}^s \mathcal{L}_i$:

1) $\mathcal{L} = \sum\limits_{i=1}^s \mathcal{L}_i$ и $\dim\mathcal{L} = \sum\limits_{i=1}^s \dim\mathcal{L}_i$

2) Объединение базисов $\mathcal{L}_1, ..., \mathcal{L}_s$ является базисом в $\mathcal{L}$

**Лемма 1**: $[\mathcal{L} = \text{Ker} \mathcal{A} \oplus \text{Im} \mathcal{A}] \Leftrightarrow [\text{Ker} \mathcal{A} = \text{Ker} \mathcal{A}^2]$

$\square$

Рассмотрим подпротсранство $\mathcal{W} = \text{Ker} \mathcal{A} + \text{Im} \mathcal{A}$

По формуле Грассмана $\dim(\mathcal{W}) = \dim\text{Ker} \mathcal{A} + \dim\text{Im} \mathcal{A} - \dim(\text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A})$

Из курса линейной алгебры известно:

1) $\dim\text{Ker} \mathcal{A} + \dim\text{Im} \mathcal{A} = \dim\mathcal{L}$

2) Если $\mathcal{L}' \subset \mathcal{L}$, то $[\mathcal{L}' = \mathcal{L}] \Leftrightarrow [\dim\mathcal{L}' = \dim\mathcal{L}]$

Теперь пользуясь первым из определений прямой суммы, можно переписать утверждение леммы в виде:

$[\text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A} = \{0\}] \Leftrightarrow [\text{Ker} \mathcal{A} = \text{Ker} \mathcal{A}^2]$

Пусть $\text{Ker} \mathcal{A} = \text{Ker} \mathcal{A}^2$, выберем любой $x \in \text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A}$, тогда $x \in \text{Im} \mathcal{A} \Rightarrow \exists z: \mathcal{A}z = x \Rightarrow \mathcal{A}^2 z = \mathcal{A}x = 0$

То есть $z \in \text{Ker} \mathcal{A} = \text{Ker} \mathcal{A}^2 \Rightarrow x = \mathcal{A}z = 0 \Rightarrow \text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A} = \{0\}$

Обратно пусть $\text{Ker} \mathcal{A} \cap \text{Im} \mathcal{A} = \{0\} \Rightarrow \forall x \in \text{Im} \mathcal{A}: x = 0 \Leftrightarrow \mathcal{A}x = 0$

Выберем любой $z \in \mathcal{L} \Rightarrow \mathcal{A}z \in \text{Im} \mathcal{A}$, получается $\mathcal{A}z = 0 \Leftrightarrow \mathcal{A}^2 z = 0$

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

Следствие: Собственные векторы, отвечающие попарно различным собственным значениям, линейно независимы, так как лежат в разных корневых подпространствах

**Теорема 5**: Существует базис в котором $A = \text{diag}(A|_{\mathcal{V}_{\lambda_1}}, ..., A|_{\mathcal{V}_{\lambda_s}})$

$\square$

Выберем в $\mathcal{V}_{\lambda_k}$ базис $e^{(k)}_{1}, ..., e^{(k)}_{n_{\lambda_k}}, k = \overline{1,s}$

В силу **теоремы 4** объединение базисов $e^{(1)}_{1}, ..., e^{(1)}_{n_{\lambda_1}}, ..., e^{(s)}_{1}, ..., e^{(s)}_{n_{\lambda_s}}$ - базис в $\mathcal{L}$

Но из **леммы 2** следует, что в этом базисе матрица преобразования имеет необходимый вид

$\blacksquare$

Из курса линейной алгебры известно, что для любого линейного преобразования линейного пространства над полем $\mathbb{C}$ существует базис в котором матрица этого преобразования является верхней треугольной

Пусть $e^{(k)}_{1}, ..., e^{(k)}_{n_{\lambda_k}}, k = \overline{1,s}$ в **теореме 5** именно такие базисы, тогда характеристическое уравнение имеет вид $(\lambda - \lambda_1)^{n_{\lambda_1}}...(\lambda - \lambda_s)^{n_{\lambda_s}} = 0$

Следствие: размерности корневых подпространств равны алгебралическим кратностям соответсвующих собственных значений в характеристическом уравнении

# Циклические подпространства

Выберем корневое подпространтсво $\mathcal{K} = \mathcal{V}_{\lambda} \neq \{0\}$

Будем рассматривать преобразование $\mathcal{B} = \mathcal{A}_\lambda|_\mathcal{K}$

В силу свойств корневых подпространств $\mathcal{B}$ является нильпотентным с показателем $h_\lambda$, то есть $\mathcal{B}^{h_\lambda} = \Theta$

**Определение 7**: Если $x \in \mathcal{K}: h = h_\lambda(x) > 1$, то $x$ называют $(h-1)$-ым присоединённым вектором к собственному вектору $e = \mathcal{B}^{h-1}x$

**Определение 8**: Упорядоченный набор $e^{(0)} = \mathcal{B}e^{(1)}, e^{(1)} = \mathcal{B}e^{(2)}, ..., e^{(h-2)} = \mathcal{B}e^{(h-1)}, e^{(h-1)} = x: h_\lambda(x) = h$ называется жордановой цепочкой высоты $h$

Свойства цепочек:

1) Цепочки состоят из одного собственного вектора $e^{(0)}$ и $(h-1)$-го присоединённого вектора

2) Из **теоремы 2** следует, что векторы одной цепочки линейно независимы

**Определение 9**: Пусть $e^{(0)}, ..., e^{(h-1)}$ - жорданова цепочка, тогда $\mathcal{Y} = \langle e^{(0)}, ..., e^{(h-1)} \rangle$ называют циклическим подпространтсвом

**Лемма 3**: $\mathcal{Y}$ - подпространство инвариантное относительно $\mathcal{A}$

$\square$

$k = \overline{1, h-1}: \mathcal{A} e^{(k)} = \mathcal{A}_\lambda e^{(k)} + \lambda e^{(k)} = e^{(k-1)} + \lambda e^{(k)} \in \mathcal{Y}$

$k = 0: \mathcal{A} e^{(k)} = \mathcal{A} e^{(0)} = \lambda e^{(0)} \in \mathcal{Y}$

$\blacksquare$

Следствие: силу второго свойства жордановых цепочек векторы $e^{(0)}, ..., e^{(h-1)}$ образуют базис в $\mathcal{Y}$ и матрица ограничения имеет вид

$A|_\mathcal{Y} = J_h(\lambda) = \left(
\begin{array}{cccccc}
\lambda & 1       &  0     & \dots  &    0    & 0      \\
0       & \lambda &  1     & \ddots &  \vdots & \vdots \\
0       &      0  & \ddots & \ddots &  0      &      0 \\
\vdots  &  \vdots & \ddots & \lambda& 1       &  0     \\
0       &      0  &  \dots &    0   & \lambda & 1      \\
0       &      0  &  \dots &    0   &      0  & \lambda
\end{array}
\right) \in \mathbb{C}^{h \times h}$

**Определение 10**: Матрица $J_h(\lambda)$ называется жордановой клеткой порядка $h$ с собственным значением $\lambda$

**Лемма 4**: Если жордановы цепочки построены на линейно независимых собственных векторах, соответствующих одному и тому же собственному значению, то векторы этих цепочек линейно независимы в совокупности

$\square$

Рассмотрим систему векторов $\tilde{e}$, состоящую из цепочек $e^{(0)}_1, ..., e^{(h_1-1)}_1, ..., e^{(0)}_d, ..., e^{(h_d-1)}_d$ с высотами $h_i, i = \overline{1, d}$

$m = h_1 + ... + h_d$ - количество векторов в $\tilde{e}$

Теперь пронумеруем векторы $\tilde{e}$ следующим образом

$f_1 = e^{(0)}_1, ..., f_d = e^{(0)}_d, f_{d+1}, ..., f_m$

То есть первые $d$ векторов собственные, а оставшиеся векторы - присоединённые, занумерованные в произвольном порядке

Покажем, что векторы $\tilde{e}$ линейно независимы индукцией по максимальной высоте цепочек $h = \max\limits_i h_i$

При $h = 1$ получаум, что $\tilde{e}$ состоит только из векторов $e^{(0)}_1, ..., e^{(0)}_d$, которые независимы по условию теоремы

Пусть верно при $h \le H$, докажем для $h = H + 1$, для этого рассмотрим линейную комбинацию, зануляющую систему $\tilde{e}$

$\sum\limits_{i=1}^m \alpha_i f_i = 0 \Rightarrow \sum\limits_{i=1}^m \alpha_i \mathcal{B} f_i = 0 \Rightarrow \sum\limits_{i=d+1}^m \alpha_i \mathcal{B} f_i = 0$, где $h(\mathcal{B} f_i) \le H$

Получается, что по предположению индукции коэффициенты $\alpha_{d+1}, ..., \alpha_m$ обязаны быть равными нулю, но оставшиеся коэффициенты $\alpha_1, ..., \alpha_d$ стоят при собственных векторах, следовательно тоже равны нулю

$\blacksquare$

**Теорема 6**: $\mathcal{K} = \bigoplus\limits_{i=1}^d \mathcal{Y}_i$, где $\mathcal{Y}_i$ - циклические подпространства

$\square$

$\mathcal{B}: \mathcal{K} \rightarrow \mathcal{K} \Rightarrow \mathcal{B}(\mathcal{K}) \subset \mathcal{K} \Rightarrow \mathcal{B}^2(\mathcal{K}) \subset \mathcal{B}(\mathcal{K}) \subset \mathcal{K} \Rightarrow ...$

Но $\mathcal{B}$ - нильпотентный с показателем $m = h_\lambda$, поэтому

$\{0\} = \mathcal{B}^m(\mathcal{K}) \subset \mathcal{B}^{m-1}(\mathcal{K}) \subset ... \subset \mathcal{B}(\mathcal{K}) \subset \mathcal{K}$

Определим $\mathcal{W}_p = \mathcal{B}^p(\mathcal{K}) \cap \text{Ker}\mathcal{B}, \;\; p = \overline{1,m}$

$\{0\} = \mathcal{W}_m \subset \mathcal{W}_{m-1} \subset ... \subset \mathcal{W}_1 \subset \text{Ker}\mathcal{B}$

Обозначим $d = \dim\text{Ker}\mathcal{B}$ и будем строить базис в $\text{Ker}\mathcal{B}$ следующим образом: сначала выберем базис в $\mathcal{W}_{m-1}$ затем дополним его до базиса в $\mathcal{W}_{m-2}$ и так далее

Получается $e^{(0)}_1, ..., e^{(0)}_d$ - базис в $\text{Ker}\mathcal{B}$, такой что любой вектор из $\mathcal{W}_i$ раскладывается по векторам базиса из $\mathcal{W}_i$

Дополним каждый из векторов $e^{(0)}_i$ до жордановых цепочек максимально возможной высоты $h_i$

Далее объединив все эти цепочки получим систему векторов $e^{(0)}_1, ..., e^{(h_1-1)}_1, ..., e^{(0)}_d, ..., e^{(h_d-1)}_d$, которую обозначим $\tilde{e}$

Но $e^{(0)}_1, ..., e^{(0)}_d$ - базис в $\text{Ker}\mathcal{B} \Rightarrow$ верна **лемма 4** $\Rightarrow$ векторы системы $\tilde{e}$ линейно независимы

Полноту ситемы докажем индукцией по высоте $h = h(x), x \in \mathcal{K}$:

$h = 1 \Rightarrow x \in \text{Ker}\mathcal{B} \Rightarrow x$ раскладывается по $e^{(0)}_1, ..., e^{(0)}_d$

Пусть верно при $h \le H$, докажем для $h = H + 1$, рассмотрим $x \in \mathcal{K}: h(x) = H+1$, тогда $\mathcal{B}^Hx \in \mathcal{W}_H$

Обозначим $p = \dim\mathcal{W}_H \Rightarrow \mathcal{B}^Hx = \sum\limits_{i=1}^p \alpha_i e^{(0)}_i = \sum\limits_{i=1}^p \alpha_i \mathcal{B}^H e^{(H)}_i$

Рассмотрим $y = x - \sum\limits_{i=1}^p \alpha_i e^{(H)}_i \Rightarrow \mathcal{B}^H y = 0\Rightarrow h(y) \le H$

В силу предположения индукции получаем $x = y + \sum\limits_{i=1}^p \alpha_i e^{(H)}_i$, где $y$ раскладывается по $\tilde{e}$

То есть $\tilde{e}$ - базис в $\mathcal{K}$ и $\mathcal{K} = \bigoplus\limits_{i=1}^d \langle e^{(0)}_i, ..., e^{(h_i-1)}_i \rangle$

$\blacksquare$

# Теорема Жордана

**Определение 11**: Квадратные матрицы $A$ и $B$ называются подобными, если $\exists$ невырожденная $S: S^{-1}AS = B$ 

Подобные матрицы будем обозначать $A \sim B$

Матрицы подобны тогда и только тогда, когда они являются матрицами одного и того же преобразования, но возможно в разных базисах

**Определение 12**: Матрица $J = \text{diag}(J_{k_1}(\lambda_1), J_{k_2}(\lambda_2), ..., J_{k_m}(\lambda_m))$, где $k_1 + ... + k_m = n$ и $\lambda_k$ могут повторяться, называется жордановой матрицей

**Определение 13**: Если $J \sim A$, то говорят, что $J$ - жорданова (нормальная) форма матрицы $A$

**Теорема 7**: Для любого линейного преобразования $\mathcal{A}$ линейного пространства $\mathcal{L}$ над полем $\mathbb{C}$ существует базис, в котором матрица преобразования $A$ имеет жорданову форму

$\square$

Пусть $\mu_1, ..., \mu_s$ - собственные значения $\mathcal{A}$, тогда по **теореме 4** имеет место представление $\mathcal{L} = \bigoplus\limits_{i=1}^s \mathcal{K}_i$, где $\mathcal{K}_i = \mathcal{V}_{\mu_i}$ - соответствующие корневые подпространства

В силу **теоремы 6**: $\mathcal{K}_i = \bigoplus\limits_{p=1}^{d_i} \mathcal{Y}_p^{(i)}$, где $\mathcal{Y}_p^{(i)}$ - циклические подпространства с собственным значением $\mu_i$

Обозначим $k(i, p) = \dim\mathcal{Y}_p^{(i)} \Rightarrow \sum\limits_{i=1}^s \sum\limits_{p=1}^{d_i} k(i, p) = n$

По следствию из **леммы 3** в $\mathcal{Y}_p^{(i)}$ можно выбрать такой базис, что $A|_{\mathcal{Y}_p^{(i)}} = J_{k(i, p)}(\mu_i)$

Выбрав в $\mathcal{K}_i$ базис как объединение базисов в состовляющих его циклических подпространствах, получаем

$A|_{\mathcal{K}_i} = \text{diag}(J_{k(i, 1)}(\mu_i), ..., J_{k(i, d_i)}(\mu_i))$

Далее как и в **теореме 5** возьмём в качестве базиса в $\mathcal{L}$ объединение базисов корневых подпространств $\mathcal{K}_1, ..., \mathcal{K}_s \Rightarrow A = \text{diag}(A|_{\mathcal{K}_1}, ..., A|_{\mathcal{K}_s})$

$\blacksquare$

**Определение 14**: базис из **теоремы 7** называют жордановым базисом

# Единственность жордановой формы

**Лемма 5**: Отношение подобия матриц $\sim$ является отношением эквивалентности

$\square$

1) Рефлексивность: $\exists S = E: A = S^{-1}AS \Rightarrow A \sim A$

2) Симметричность: $A \sim B \Rightarrow \exists S: S^{-1}AS = B \Rightarrow SBS^{-1} = A \Rightarrow B \sim A$

3) Транзитивность: $A \sim B, B \sim C \Rightarrow \exists S,P: S^{-1}AS = B, P^{-1}BP = C \Rightarrow \exists R = SP: R^{-1}AR = C \Rightarrow A \sim C$  

$\blacksquare$

Следствие: Пусть $J_A$ - жорданова форма $A$ и $J_B$ - жорданова форма $B$, тогда $[A \sim B] \Leftrightarrow [J_A \sim J_B]$

Рассмотрим матрицу $S$, переставляющую местами $i$-й и $j$-й столбцы, тогда умножение на эту же матрицу слева будет менять местами соотвествубщие строки

Кроме того очевидно $S^{-1} = S \Rightarrow S^{-1}AS$ - матрица в которой строки и стоблцы с $i$-ым и $j$-ым номером поменяли местами

Пусть $J$ - жорданова матрица, тогда последовательность рассмотренных выше переходов позволяет менять её блоки местами

**Теорема 8**: $[$Жордановы матрицы $J_1$ и $J_2$ эквивалентны$] \Leftrightarrow [J_1$ и $J_2$ отличаются лишь порядком блоков, но сами жордановы клетки одинаковые$]$

$\square$

Достаточность следует из предшествовавших теореме размышлений

Докажем необходимость:

...

$\blacksquare$

Следствие: Все жордановы формы матрицы $A$ одинаковые с точностью до порядка блоков

$\square$

Пусть $J_1, J_2$ - жордановы формы $A \Leftrightarrow J_1 \sim A$ и $J_2 \sim A$

По **лемме 5** получаем $J_1 \sim J_2$

**Теорема 8** заканчивает доказательство

$\blacksquare$

# Нахождение корневых векторов

**Теорема 7** говорит о существовании базиса, в котором матрица преобразования $\mathcal{A}$ - жорданова, для нахождения такого базиса необходимо:

0) Выбрать произвольный базис в котором мы будем работать

1) Найти собственные значения $\mathcal{A}$ и размерности его корневых подпространств

По следствию из **теоремы 5** для этого достаточно найти все корни хар уравнения ${\Large\chi}_{\mathcal{A}}(\lambda) = 0$ с учётом их кратности

Далее для каждго из корневых подпространств $\mathcal{V}_\lambda: \mathcal{V}_\lambda = n_\lambda$ нужно

2) Отыскать базис в собственном подпространстве $\mathcal{L}_\lambda \subset \mathcal{V}_\lambda$

Для этого достаточно найти фундаментальную систему решений для $(A - \lambda E)x = 0$

В общем случае $r_\lambda = \dim\mathcal{L}_\lambda < n_\lambda$

3) Получить недостающие $n_\lambda-r_\lambda$ присоединённых векторов

Здесь есть несколько вариантов: либо честно искать $\mathcal{W}_p$ как в **теореме 6** и уже к ним вычислять присоединённые векторы, либо пытаться сразу искать присоединённые векторы к линейным комбинациям базисных векторов $\mathcal{L}_\lambda$

# Подобие матрицы и её транспонированной

Начнём с рассмотрения антидиагональной матрицы $S_k = \left(
\begin{array}{ccccc}
  &   &   &   & 1 \\
  & {\huge O} &   & 1 &   \\
  &   & ⋰ &   &   \\
  & 1 &   & {\huge O} &   \\
1 &   &   &   &   \\
\end{array}
\right) \in \mathbb{C}^{k \times k}$

Умножение на такую матрицу справа переставляет столбцы в обратном порядке, умножение слева - строки

**Теорема 9**: Для любой матрицы $A \in \mathbb{C}^{k \times k}$ верно $A \sim A^T$

$\square$

Для начала рассмотрим жорданову клетку $J_k(\lambda)$

$S_k^{-1} = S_k \Rightarrow S_k^{-1}J_k(\lambda)S_k = S_kJ_k(\lambda)S_k = J_k(\lambda)^T \Rightarrow J_k(\lambda) \sim J_k(\lambda)^T$

Теперь рассмотрим жорданову матрицу $J = \text{diag}(J_{k_1}(\lambda_1), J_{k_2}(\lambda_2), ..., J_{k_m}(\lambda_m)) \in \mathbb{C}^{n \times n}$

$S_n^{-1}JS_n = S_nJS_n = \text{diag}(J_{k_m}(\lambda_m)^T, J_{k_{m-1}}(\lambda_{m-1})^T, ..., J_{k_1}(\lambda_1)^T) = \tilde{J} \Rightarrow J \sim \tilde{J}$

В силу **теоремы 8** получается $\tilde{J} \sim \text{diag}(J_{k_1}(\lambda_1)^T, J_{k_2}(\lambda_2)^T, ..., J_{k_m}(\lambda_m)^T) = J^T\Rightarrow J \sim J^T$

Пусть теперь $J$ - жорданова форма матрицы $A$, тогда

$\exists P: A = P^{-1}JP \Rightarrow A^T = P^TJ^T(P^T)^{-1} \Rightarrow A^T \sim J^T$

Окончательно $A \sim J \sim J^T \sim A^T$

$\blacksquare$
