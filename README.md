// sum_of_different_series
#include<stdio.h>
#include<math.h>
#include<stdlib.h>
void sum_n_num();
void sum_fact_num();
void sum_reciprocal();
void fact_by_num();
void sum_of_sq();
void main()
{
    int ch;
    while(1){
    printf("\n1.sum of n numbers.\n2.sum of factorials.\n3.sum of reciprocals\n4.(n!/n).\n5.sum of square of n numbers.\n");
    printf("enter your choice:");
    scanf("%d",&ch);
    switch(ch)
    {
        case 1:sum_n_num();
        break;
        case 2:sum_fact_num();
        break;
        case 3:sum_reciprocal();
        break;
        case 4: fact_by_num();
        break;
        case 5:sum_of_sq();
        break;
        default:
        printf("invalid choice");
    }
    }
   
}
void sum_n_num()
{
    int n,i,sum=0;
    printf("enter a number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++){
        sum+=i;
    }
    printf("sum=%d\n",sum);
}
void sum_fact_num(){
     int n,i,fact=1,sum=0;
    printf("enter the number\n");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        fact=fact*i;
        sum+=fact;
    }
    printf("sum= %d\n",sum);
}
void sum_reciprocal(){
    float n,i;
    float sum=0,h;
    printf("enter number:");
    scanf("%f",&n);
    for(i=1;i<=n;i++){
        h=(1/i);
        sum+=h;
    }
    printf("sum=%f\n",sum);
}
void fact_by_num(){
     int n;
   float i,fact=1,y,res;
  printf("enter the number:");
  scanf("%d",&n);
  for(i=1;i<=n;i++)
  {
      y=(fact*=i);
      res=y/n;
  }
  printf("(%d!/%d)=%.2f\n",n,n,res);
}
void sum_of_sq(){
    int n,i,sum=0,y;
    printf("enter the number:");
    scanf("%d",&n);
    for(i=1;i<=n;i++)
    {
        y=pow(i,2);
        sum+=y;
    }
    printf("sum=%d\n",sum);
}
