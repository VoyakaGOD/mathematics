Суммирование по правилу Эйнштейна подразумевается только для латинских букв.

Суммирование подразумевается при любом количестве повторяющихся индексов.

# Градиент в ортогональных криволинейных координатах

$$\newcommand{\dd}[2]{\frac{\partial #1}{\partial #2}}$$
$$\newcommand{\d}{\mathrm{d}}$$

$\vec{r} = (x_1, x_2, x_3)^T \in \R^3$

$\vec{q} = (q_1, q_2, q_3)^T \in \R^3$

Криволинейные координаты задаются следующим образом $\vec{r} = \vec{r}(\vec{q})$

Градиент в прямолинейных координатах $\nabla f = (\dd{f}{x_1}, \dd{f}{x_2}, \dd{f}{x_3}) = \dd{f}{x_i}$

$\d f = \dd{f}{x_i}\d x_i = (\nabla f, \d \vec{r}) = (\nabla f, \dd{\vec{r}}{q_i})\d q_i$

$H_i\vec{e}_i = \dd{\vec{r}}{q_i}, \; |\vec{e}_i| = 1$

Коэффициенты Ламе $H_i \triangleq |\dd{\vec{r}}{q_i}|$

Таким образом $(\nabla f, \vec{e}_\alpha) = \frac{1}{H_\alpha}\dd{f}{q_\alpha}$

Далее считаем координаты ортогональными $(\vec{e}_i, \vec{e}_j) = 0$

В этом случае $\boxed{\nabla f = (\nabla f, \vec{e}_i)\vec{e}_i = \frac{1}{H_i}\dd{f}{q_i}\vec{e}_i}$