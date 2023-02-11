# 2023-02-11-ROKA
Not completed (2023-02-11 Backjoon 1081 title : sum)

#include <stdio.h>

int sum = 0;

int main()
{
  int j = 1;
  while(j) {
    int i,k = 0;
      scanf("%d %d", &i, &k);
      if(((i >= 0) && (i <= 2000000000)) && ((k >= 0) && (k <= 2000000000))) {
        if((i > 99) || (k > 99))
          if((i > 9) || (k > 9)) {
            for(int q = i; q <= k; q++) { // 항상 i는 k보다 크다는 조건을 만족해야함.
              sum += q % 10;
            }
          }
        }
      else
        break;
  }
      printf("범위를 넘었기 때문에 종료이며 더해진값은 %d이다.\n", sum);
    return 0;
}

// 2000000000 % 1000000000
// 2000000000 % 100000000
// 2000000000 % 10000000
// 2000000000 % 1000000
// 2000000000 % 100000
// 2000000000 % 10000
// 2000000000 % 1000
// 2000000000 % 100
// 2000000000 % 10
// 2000000000 % 1

// if(i <10 i<100 i<1000 i<10000 i<100000 i<1000000 i<10000000 i<100000000 i<1000000000)




#include <stdio.h>

int one = 0;
int ten = 0;
int number100 = 0;
int number1000 = 0;
int number10000 = 0;
int number100000 = 0;
int number1000000 = 0;
int number10000000 = 0;
int number100000000 = 0;
int number1000000000 = 0;
// 23:35분 연등끝내기전 => 서로다른 자리수의 합을 모르겠다...

int main()
{
  int j = 1;
  while(j) {
    int i,k = 0;
      scanf("%d %d", &i, &k);
      if(((i >= 0) && (i <= 2000000000)) && ((k >= 0) && (k <= 2000000000))) {
          if((i < 10)) { // i가 1이고 k가 100일때 밑에있는 if문으로 못감
            if(k < 10) {
              for(int q = i; q <= k; q++) { // 항상 i는 k보다 크다는 조건을 만족해야함
                ten += q % 10;
                }
                 printf("%d\n", one+ten);
            }
          }
          else if((i < 100)) {
            if(k < 100) {
            for(int q = i; q <= k; q++) {
              one += q % 10;
              ten += q / 10;
              }
               printf("%d\n", one+ten);
              }
            else {
             if(k < 1000) {
            for(int q = i; q <= k; q++) {
              number100 += q / 100;
              ten += (q / 10) / 10;
              one += q % 10;
              }
                printf("%d\n", number100+one+ten);
              }
              }
            }
          else if((i < 1000)) {
            if(k < 1000) {
             for(int q = i; q <= k; q++) {
              number100 += q / 100;
              ten += (q / 10) / 10;
              one += q % 10;
               }
                printf("%d\n", number100+one+ten);
              }
            }
          else if((i < 10000)) {
            if(k < 10000) {
             for(int q = i; q <= k; q++) {
              number1000 += (q / 1000) / 1000;
              number100 += (q / 100) / 100;
              ten += (q / 10) / 10;
              one += q % 10;
               }
                printf("%d\n", number1000+number100+one+ten);
              }
            }
          else if((i < 100000)) {
            if(k < 100000) {
             for(int q = i; q <= k; q++) {
              number10000 += q / 10000;
              number1000 += (q / 1000) / 1000;
              number100 += (q / 100) / 100;
              ten += (q / 10) / 10;
              one += q % 10;
               }
               printf("%d\n", number10000+number1000+number100+one+ten);
              }
            else {
              if(k < 2000000000) {
             for(int q = i; q <= k; q++) {
              number100000000 += q / 100000000;
              number10000000 += (q / 10000000) / 10000000;
              number1000000 += (q / 1000000) / 1000000;
              number100000 += (q / 100000) / 100000;
              number10000 += (q / 10000) / 10000;
              number1000 += (q / 1000) / 1000;
              number100 += (q / 100) / 100;
              ten += (q / 10) / 10;
              one += q % 10;
               }
          printf("%d\n", number100000000+number10000000+number1000000+number100000+number10000+number1000+number100+one+ten);
              }
            }
            }
          else if((i < 1000000)) {
            if(k < 1000000) {
             for(int q = i; q <= k; q++) {
              number100000 += q / 100000;
              number10000 += q / 10000;
              number1000 += q / 1000;
              number100 += q / 100;
              ten += q / 10;
              one += q % 10;
               printf("%d\n", number100000+number10000+number1000+number100+one+ten);
                }
              }
            }
          else if((i < 10000000)) {
            if(k < 10000000) {
             for(int q = i; q <= k; q++) {
              number1000000 += q / 1000000;
              number100000 += q / 100000;
              number10000 += q / 10000;
              number1000 += q / 1000;
              number100 += q / 100;
              ten += q / 10;
              one += q % 10;
        printf("%d\n", number1000000+number100000+number10000+number1000+number100+one+ten);
                }
              }
            }
          else if((i < 100000000)) {
            if(k < 100000000) {
             for(int q = i; q <= k; q++) {
              number10000000 += q / 10000000;
              number1000000 += q / 1000000;
              number100000 += q / 100000;
              number10000 += q / 10000;
              number1000 += q / 1000;
              number100 += q / 100;
              ten += q / 10;
              one += q % 10;
        printf("%d\n", number10000000+number1000000+number100000+number10000+number1000+number100+one+ten);
               }
              }
            }
          else if((i < 2000000000)) {
            if(k < 2000000000) {
             for(int q = i; q <= k; q++) {
              number100000000 += q / 100000000;
              number10000000 += q / 10000000;
              number1000000 += q / 1000000;
              number100000 += q / 100000;
              number10000 += q / 10000;
              number1000 += q / 1000;
              number100 += q / 100;
              ten += q / 10;
              one += q % 10;
          printf("%d\n", number100000000+number10000000+number1000000+number100000+number10000+number1000+number100+one+ten);
                }
              }
            }
          else
            printf("아직모름");
            break;
        }
      else
        break;
  }
    return 0;
}

// 2000000000 % 1000000000
// 2000000000 % 100000000
// 2000000000 % 10000000
// 2000000000 % 1000000
// 2000000000 % 100000
// 2000000000 % 10000
// 2000000000 % 1000
// 2000000000 % 100
// 2000000000 % 10
// 2000000000 % 1

// if(i <10 i<100 i<1000 i<10000 i<100000 i<1000000 i<10000000 i<100000000 i<1000000000)

// 여기서 신경써줘야하는 조건이 1.각 자리수별로 더하는 것 2.조건문을 만들때 공통된 조건이 있으면 전부다 만족한다는것 총 이십억


//여기서 값의 자리수가 다른조건을 만족하는 합의값을 신경써야한다
