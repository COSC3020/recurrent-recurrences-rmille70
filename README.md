[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/8KYthzwp)
# Recurrent Recurrences

Give big $\Theta$ bounds for the following recurrence relations.

1.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

$T(n) = T(\frac{n}{13}) + 5$

$T(n) = T(\frac{n}{13^2}) + \frac{5}{13} + 5$

$T(n) = T(\frac{n}{13^3}) + \frac{5}{13^2} +\frac{5}{13} + 5$

$T(n) = T(\frac{n}{13^i}) + \sum\limits_{j=0}^{i-1} \frac{5}{13^j}$    { where $i = \log_{13}(n)$ }

$T(n) = 1 + \frac{5}{13^2} +\frac{5}{13} + 5$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$
