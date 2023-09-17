// Rock, Paper, Scissor Game In C language

#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main()
{
    char name[50];
    int game, no;
    int p1 = 0, p2 = 0;
    printf("Enter Player name: ");
    scanf("%s", &name);
    printf("You can enter only number for,\nRock = 1\nPaper = 2\nScissors = 3\n");

    for (int i = 0; i < 3; i++)
    {
        printf("It's Your turn %s\n", name);
        scanf("%d", &no);
        srand(time(NULL));
        game = rand() % 3;
        if (no == 1)
        {
            if (no == game)
            {
                printf("Drawn\n");
            }
            else if (game == 2)
            {
                printf("Computer wins 1 point\n");
                p2++;
            }
            else
            {
                printf("%s wins 1 point\n", name);
                p1++;
            }
        }
        else if (no == 2)
        {
            if (no == game)
            {
                printf("Drawn\n");
            }
            else if (game == 3)
            {
                printf("Computer wins 1 point\n");
                p2++;
            }
            else
            {
                printf("%s wins 1 point\n", name);
                p1++;
            }
        }
        else if (no == 3)
        {
            if (no == game)
            {
                printf("Drawn\n");
            }
            else if (game == 1)
            {
                printf("Computer wins 1 point\n");
                p2++;
            }
            else
            {
                printf("%s wins 1 point\n", name);
                p1++;
            }
        }
        else
        {
            printf("You Entered wrong input\n");
        }
        printf("%s Point : %d\n", name, p1);
        printf("Computer's Point : %d\n", p2);
    }
    if (p1 > p2)
    {
        printf("%s Your are Winner!!!", name);
    }
    else
    {
        printf("Computer is Winner!!!");
    }
}