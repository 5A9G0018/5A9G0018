<h2>🏴‍☠️ 歡迎來到內衣大盜的世界</h2>

>- [🈚 Hi, I’m 光易旋轉跳二世](https://m.facebook.com/people/%E9%84%A7%E5%85%89%E6%98%93/100008943034216/)
>-  [👀蘇貞昌會做事](https://www.chinatimes.com/realtimenews/20221210002806-260407)

<h2>🍌 蘇格拉底的秘密</h2>

>-  [🎃給光易抄的作業](https://github.com/5A9G0018/HW10)
>-  [🀄光易旋轉跳時聽的歌](https://www.youtube.com/watch?v=KEedfZtpLio)

![5A9G0018's github stats](https://github-readme-stats.vercel.app/api?username=5A9G0018&theme=transparent)
![](https://github.com/tondrejk/tondrejk/blob/main/contributions.svg)

[我的網頁](https://5a9g0018.github.io/topic/)
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

    //排序
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

    //找出最低及格分數
    int minPass = -1;
    for (int i = 0; i < n; i++)
    {
        if (score[i] >= 60)
        {
            minPass = score[i];
            break;
        }
    }

    //找出最高不及格分數
    int maxNoPass = -1;
    for (int i = n - 1; i >= 0; i--)
    {
        if (score[i] < 60)
        {
            maxNoPass = score[i];
            break;
        }
    }

    //印出解答
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
