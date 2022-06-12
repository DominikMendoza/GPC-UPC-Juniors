![Kun y los subarreglos](https://github.com/DominikMendoza/GPC-UPC-Juniors/blob/main/imgs/a.png)

**Input Format**
$$
f(x)=\left\{
\begin{array}{ll}
2x & \text{si }x\leq 0 \\
3x   &  \text{si }x\geq 0
\end{array}
\right.
$$

**Constraints**
```{r}
1 <= n <= 20
```

**Output Format**

Imprimir la cantidad de subarreglos que existen de tal forma que tengan todos sus elementos en orden no decreciente.

**Sample Input 0**

```{r}
4
12 10 15 12
```
**Sample Output 0**
```{r}
5
```
**Explanation 0**

Existen 5 subarreglos que cumplan lo requerido:

- El subarreglo formado por el primer elemento [12]
- El subarreglo formado por el último elemento [12]
- El subarreglo formado por el segundo elemento [10]
- El subarreglo formado por el tercer elemento [15]
- El subarreglo formado por el segundo y tercer elemento [10, 15]