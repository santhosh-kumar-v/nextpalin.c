#include<stdio.h>

int main()
{
    int n;
    scanf("%d",&n);
    nextpalindrome(n);
}
int nextpalindrome(int x)
{
    int i,rev1;
    i=x+1;
    while(i)
    {
        x=i;
        rev1=revofdigit(x);
        if(rev1==i)
        {
            break;
        }
        i++;
    }
    printf("%d",rev1);
}
int revofdigit(int y)
{
    int rem,t,rev=0;
    while(y!=0)
        {
            rem=y%10;
            rev=rem+rev*10;
            y/=10;
        }
        return rev;
    
}
