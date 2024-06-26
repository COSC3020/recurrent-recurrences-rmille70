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

Using Substitution, we find:

$T(n) = T(\frac{n}{13}) + 5$

$T(n) = T(\frac{n}{13^2}) + 5 + 5$

$T(n) = T(\frac{n}{13^3}) + 5 + 5 + 5$

$T(n) = T(\frac{n}{13^i}) + 5i$    { where $i = \log_{13}(n)$ }

$T(n) = 1 + 5(\log_{13}(n))$

Thus the completity is $\Theta(\log_{13}(n))$

2.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 5 & n > 1
    \end{cases}
$$

Using Substitution, we find:

$T(n) = 13T(\frac{n}{13}) + 5$

$T(n) = 13^2T(\frac{n}{13^2}) + 5(13) + 5$

$T(n) = 13^3T(\frac{n}{13^3}) + 5(13^2) + 5(13) + 5$

$T(n) = 13^iT(\frac{n}{13^i}) + 5\sum\limits_{j=0}^{i-1} 13^j$    { where $i = \log_{13}(n)$ }

$T(n) = n + 5(\frac{1-13^{\log_{13}(n)}}{1-13})$

$T(n) = n + 5(\frac{1-13^{\log_{13}(n)}}{1-13})$

$T(n) = n + \frac{5n-5}{12}$

Thus the complexity is $\Theta(n)$ since n is the leading term.

3.
$$ T(n) =
    \begin{cases}
        1 & n \leq 1\\
        13 T\left(\frac{n}{13}\right) + 2n & n > 1
    \end{cases}
$$

Using Substitution, we find:

$T(n) = 13T(\frac{n}{13}) + 2n$

$T(n) = 13(13T(\frac{n}{13^2}) + (\frac{2n}{13})) + 2n$

$T(n) = 13^2T(\frac{n}{13^2}) + 2n + 2n$

$T(n) = 13(13^2T(\frac{n}{13^3}) + \frac{2n}{13} + \frac{2n}{13}) + 2n$

$T(n) = 13^3T(\frac{n}{13^3}) + 2n + 2n + 2n$

$T(n) = 13^iT(\frac{n}{13^i}) + i(2n)$    { where $i = \log_{13}(n)$ }

$T(n) = n + 2n\log_{13}(n)$

Thus the complexity is $\Theta(n\log_{13}(n))$ since $2n\log_{13}(n)$ is the leading term.