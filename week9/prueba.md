![Kun y los subarreglos](https://github.com/DominikMendoza/GPC-UPC-Juniors/blob/main/imgs/a.png)

# Kun y los subarreglos
**Input Format**

La primera línea contiene un entero ```n``` , indicando la cantidad de elementos del arreglo.

La segunda línea contiene los A<sub>i</sub>  números enteros  que forman el arreglo.

**Constraints**

1 ```<=``` n ```<=``` 20

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
---

## Solución

```c++
#include <bits/stdc++.h>
using namespace std;

long long getfacto(int n)
{
    return ((n * (n + 1))/ 2);
}
int main()
{
    vector<int> cer;
    int n;
    cin >> n;
    int nums[n];
    for (int i = 0; i < n; i++)
    {
        cin >> nums[i];
    }
    int cont = 1;
    for (int i = 0; i < n - 1; i++)
    {
        if (nums[i] <= nums[i + 1])
        {
            cont++;
        }
        else
        {
            cer.push_back(cont);
            cont = 1;
        }
    }
    if (nums[n - 2] <= nums[n - 1]) cer.push_back(cont);
    else cer.push_back(1);
    long long suma = 0;
    for (size_t i = 0; i < cer.size(); i++)
    {
        suma += getfacto(cer.at(i));
    }
    cout << suma;
    return 0;
}
```