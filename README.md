<h2>π΄ββ οΈ ζ­‘θΏδΎε°ε§θ‘£ε€§ηηδΈη</h2>

>- [π Hi, Iβm εζζθ½θ·³δΊδΈ](https://m.facebook.com/people/%E9%84%A7%E5%85%89%E6%98%93/100008943034216/)
>-  [πθθ²ζζεδΊ](https://www.chinatimes.com/realtimenews/20221210002806-260407)

<h2>π θζ ΌζεΊηη§ε―</h2>

>-  [πη΅¦εζζηδ½ζ₯­](https://github.com/5A9G0018/HW10)
>-  [πεζζθ½θ·³ζθ½ηζ­](https://www.youtube.com/watch?v=KEedfZtpLio)

![5A9G0018's github stats](https://github-readme-stats.vercel.app/api?username=5A9G0018&theme=transparent)
![](https://github.com/tondrejk/tondrejk/blob/main/contributions.svg)

[ζηηΆ²ι ](https://5a9g0018.github.io/topic/)
```cpp
#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    int n;
    scanf("%d", &n);

    int score[n];
    for (int i = 0; i < n; i++)
    {
        scanf("%d", &score[i]);
    }

    //ζεΊ
    for (int i = 0; i < n - 1; i++)
    {
        for (int j = i + 1; j < n; j++)
        {
            if (score[i] > score[j])
            {
                score[i] = score[i] ^ score[j];
                score[j] = score[i] ^ score[j];
                score[i] = score[i] ^ score[j];
            }
        }
    }

    //ζΎεΊζδ½εζ ΌεζΈ
    int minPass = -1;
    for (int i = 0; i < n; i++)
    {
        if (score[i] >= 60)
        {
            minPass = score[i];
            break;
        }
    }

    //ζΎεΊζι«δΈεζ ΌεζΈ
    int maxNoPass = -1;
    for (int i = n - 1; i >= 0; i--)
    {
        if (score[i] < 60)
        {
            maxNoPass = score[i];
            break;
        }
    }

    //ε°εΊθ§£η­
    for (int i = 0; i < n; i++)
    {
        printf("%d", score[i]);
        if (i < n - 1)
        {
            printf(" ");
        }
    }
    printf("\n");

    if (maxNoPass == -1)
    {
        printf("best case\n");
    }
    else
    {
        printf("%d\n", maxNoPass);
    }

    if (minPass == -1)
    {
        printf("worst case\n");
    }
    else
    {
        printf("%d\n", minPass);
    }

    system("pause");
    return 0;
}
```
