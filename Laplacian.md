$$\newcommand{\ddd}[2]{\frac{\partial}{\partial #1} \left( #2 \right)}$$
$$\newcommand{\dd}[2]{\frac{\partial #1}{\partial #2}}$$
$$\newcommand{\d}{\mathrm{d}}$$

# Градиент в ортогональных криволинейных координатах

$\vec{r} = (x_1, x_2, x_3)^T \in \R^3$

$\vec{q} = (q_1, q_2, q_3)^T \in \R^3$

Криволинейные координаты задаются следующим образом $\vec{r} = \vec{r}(\vec{q})$

Градиент в прямолинейных координатах $\nabla f = (\dd{f}{x_1}, \dd{f}{x_2}, \dd{f}{x_3}) = \dd{f}{x_i}$

$\d f = \dd{f}{x_i}\d x_i = (\nabla f, \d \vec{r}) = (\nabla f, \dd{\vec{r}}{q_i})\d q_i$

$H_i\vec{e}_i = \dd{\vec{r}}{q_i}, \; |\vec{e}_i| = 1$

Коэффициенты Ламе $H_i \triangleq |\dd{\vec{r}}{q_i}|$

Таким образом $(\nabla f, \vec{e}_\alpha) = \frac{1}{H_\alpha}\dd{f}{q_\alpha}$

Далее считаем координаты ортогональными $(\vec{e}_i, \vec{e}_j) = \delta_{ij}$

В этом случае $\boxed{\nabla f = (\nabla f, \vec{e}_i)\vec{e}_i = \frac{1}{H_i}\dd{f}{q_i}\vec{e}_i}$

# Дивергенция в прямолинейных координатах

В качестве определения возьмём $\nabla \vec{A} = \lim\limits_{\d(D) \to 0} \frac{1}{V}\oiint_{\partial D} \vec{A} \d \vec{S}$, где $V$ - объём области $D$, $\d(D)$ - её диаметр

Пусть в прямолинейных координатах $\vec{A} = (A_1(\vec{r}), A_2(\vec{r}), A_3(\vec{r}))^T \in \R^3$

Выберем в качестве $D$ прямоугольник со стронами $\d x_1, \d x_2, \d x_3$

Тогда $V = \d x_1 \d x_2 \d x_3$, $\oiint_{\partial D} \vec{A} \d \vec{S} = \Phi_1 + \Phi_2 + \Phi_3$

Поток через грань, пересекаемую $1$ осью, $\Phi_1 = [A_1(x_1+\d x_1, x_2, x_3) - A_1(x_1, x_2, x_3)]\d x_2 \d x_3 = \dd{A_1}{x_1}V$

Дивергенция в прямолинейных координатах $\nabla \vec{A} = \dd{A_1}{x_1} + \dd{A_2}{x_2} + \dd{A_3}{x_3} = \dd{A_i}{x_i}$

# Дивергенция в ортогональных криволинейных координатах

Перепишем в другом базисе $\vec{A} = \tilde{A}_i(\vec{q}) \vec{e}_i$, $\vec{e}_i = \frac{1}{H_i}\dd{\vec{r}}{q_i}$

Фиксируем $\d q_1, \d q_2, \d q_3$, тогда в исходном пространсте получаем фигуру похожую на параллелепипед со сторонами $h_i = H_i \d q_i$, ориентированную по векторам $\vec{e}_i$

Её объём соответственно $V = h_1 h_2 h_3 = H_1 H_2 H_3 \d q_1 \d q_2 \d q_3$

Поток аналогично распадается на 3 компорненты $\oiint_{\partial D} \vec{A} \d \vec{S} = \Phi_1 + \Phi_2 + \Phi_3$

Площадь сечения перпендикулярного к первой оси $S_1(\vec{q}) = H_2(\vec{q}) H_3(\vec{q}) \d q_2 \d q_3$

Поток через грань, пересекаемую $1$ осью, $\Phi_1 = \tilde{A}_1(q_1+\d q_1, q_2, q_3)S_1(q_1+\d q_1, q_2, q_3) - \tilde{A}_1(q_1, q_2, q_3)S_1(q_1, q_2, q_3)$

С учётом предела $\d(D) \to 0$ получаем $\Phi_1 = \ddd{q_1}{H_2 H_3 \tilde{A}_1}\d q_1 \d q_2 \d q_3$

Окончательно $\boxed{\nabla \vec{A} = \frac{1}{H_1 H_2 H_3} \ddd{q_i}{\frac{H_1 H_2 H_3}{H_i} \tilde{A}_i}}$

# Оператор Лапласа

$\Delta f = \nabla(\nabla f)$

В прямолинейных координатах $\Delta f = \dd{^2 f}{x_1^2} + \dd{^2 f}{x_2^2} + \dd{^2 f}{x_3^2} = \dd{^2 f}{x_ix_i}$

В ортогональных криволинейных координатах $\boxed{\Delta f = \frac{1}{H_1 H_2 H_3} \ddd{q_i}{\frac{H_1 H_2 H_3}{H_i^2} \dd{f}{q_i}}}$

## 1. Сферические координаты

$\vec{r} = \vec{r}(r, \theta, \varphi) = (r\sin\theta\cos\varphi, r\sin\theta\sin\varphi, r\cos\theta)^T$

$H_r = |\dd{\vec{r}}{r}| = 1$

$H_\theta = \sqrt{(r\cos\theta\cos\varphi)^2 + (r\cos\theta\sin\varphi)^2 + (r\sin\theta)^2} = r$

$H_\varphi = \sqrt{(r\sin\theta\sin\varphi)^2 + (r\sin\theta\cos\varphi)^2} = r\sin\theta$

$\Delta f = \frac{1}{r^2\sin\theta}\left[\ddd{r}{r^2\sin\theta \dd{f}{r}} + \ddd{\theta}{\sin\theta \dd{f}{\theta}} + \ddd{\varphi}{\frac{1}{\sin\theta} \dd{f}{\varphi}}\right]$

$\boxed{\Delta f = \frac{1}{r^2}\ddd{r}{r^2 \dd{f}{r}} + \frac{1}{r^2\sin\theta}\ddd{\theta}{\sin\theta \dd{f}{\theta}} + \frac{1}{r^2\sin^2\theta}\dd{^2 f}{\varphi^2}}$

## 2. Цилиндрические координаты

$\vec{r} = \vec{r}(\rho, \varphi, z) = (\rho\cos\varphi, \rho\sin\varphi, z)^T$

$H_\rho = \sqrt{\cos^2\varphi + \sin^2\varphi} = 1$

$H_\varphi = \sqrt{(\rho\sin\varphi)^2 + (\rho\cos\varphi)^2} = \rho$

$H_z = 1$

$\Delta f = \frac{1}{\rho}\left[\ddd{\rho}{\rho \dd{f}{\rho}} + \ddd{\varphi}{\frac{1}{\rho} \dd{f}{\varphi}} + \ddd{z}{\rho \dd{f}{z}}\right]$

$\boxed{\Delta f = \frac{1}{\rho}\ddd{\rho}{\rho \dd{f}{\rho}} + \frac{1}{\rho^2}\dd{^2 f}{\varphi^2} + \dd{^2 f}{z^2}}$

## 3. Полярные координаты

$\vec{r} = \vec{r}(r, \varphi) = (r\cos\varphi, r\sin\varphi)^T$

$\boxed{\Delta f = \dd{^2 f}{r^2} + \frac{1}{r}\dd{f}{r} + \frac{1}{r^2}\dd{^2 f}{\varphi^2}}$

# Ортогональная замена координат


