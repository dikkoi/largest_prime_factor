# largest_prime_factor
for project euler
#include <stdio.h>
#include <cs50.h>
#include <math.h>
    int func(void);
int main(void) {


    unsigned long num, sqwirt, i, j;
    printf ("ВВеди число: ");
    scanf ("%lu", &num);
    sqwirt = sqrt (num);
    printf ("squera root of %lu is %lu", num, sqwirt);
    int k = 0;
    for (i = sqwirt; i >=2; i--) {
        j = sqrt (i);

        int g = 0;
        for (j = sqrt (i); j>=2; j-- ) {
            if (i%j == 0) {
                //printf ("\nкорень из корня равен %lu", j);
                g++;
                //printf ("\n%d", g);
                break;
            }
        }
        if (g == 0) {
            //printf("\n%lu простое проверим как оно делит число num", i);
            if (num%i == 0) {
                printf("\n%lu делим число num без остатка", i);
                break;}
        }

    }
    func();
    return 0;
}
Возможно тут где-то пригодиться рекурсия, но мне целиком в голове не удаеться уместить всю суть алгоритма
