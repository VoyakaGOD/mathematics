Пусть $A \in \R^{n \times n}$, $B \in \R^{m \times m}$, $C \in \R^{n \times m}$

Вычислим определитель $\left|\begin{array}{ccc}A & C \\ 0 & B \end{array}\right|$

**I**) $|A| = 0 \Rightarrow$ первые $n$ столбцов матрицы $\left(\begin{array}{ccc}A & C \\ 0 & B \end{array}\right)$ линейно зависисмы $\Rightarrow \left|\begin{array}{ccc}A & C \\ 0 & B \end{array}\right| = 0 = |A| \cdot |B|$

**II**) $|A| \neq 0 \Rightarrow$ столбцы $C$ могут быть представлены как линейные комбинации столбцов $A \Rightarrow \left|\begin{array}{ccc}A & C \\ 0 & B \end{array}\right| = \left|\begin{array}{ccc}A & 0 \\ 0 & B \end{array}\right|$

Применим формулу полного разложения:

$\left|\begin{array}{ccc}A & 0 \\ 0 & B \end{array}\right| = \sum\limits_{(\alpha, \beta)} (-1)^{N(\alpha, \beta)} a_{1 \alpha_1}...a_{n \alpha_n} b_{1 \beta_1}...b_{m \beta_m}$

$\alpha = \alpha_1, ..., \alpha_n$ - перестановка $1, ..., n$

$\beta = (n + \beta_1), ..., (n + \beta_m)$ - перестановка $(n+1), ..., (n+m)$

Получается $N(\alpha, \beta) = N(\alpha)N(\beta)$

Окончательно:

$\left|\begin{array}{ccc}A & C \\ 0 & B \end{array}\right| = \sum\limits_{\alpha} (-1)^{N(\alpha)} a_{1 \alpha_1}...a_{n \alpha_n} \sum\limits_{\beta} (-1)^{N(\beta)} b_{1 \beta_1}...b_{m \beta_m} = |A| \cdot |B|$
