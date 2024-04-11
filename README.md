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

$T(n) = T(\frac{n}{13^2}) + 5 + 5$

$T(n) = T(\frac{n}{13^3}) + 5 + 5 + 5$

$T(n) = T(\frac{n}{13^i}) + i5$    { where $i = \log_{13}(n)$ }

$T(n) = 1 + 5(\log_{13}(n))$

Thus the completity is $\Theta(\log_{13}(n))$

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
