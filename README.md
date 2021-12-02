# Week-08-solutions
Count the number of sandwiches
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
     int t,x;
    scanf("%d",&t);
    for(x=0;x<t;x++)
    {
        int n,k,i,count=0,a,b;
        scanf("%d",&n);
        scanf("%d",&k);
        i=n;
        while(i>=k)
        {  a=i/k;
           b=i%k;
           count=count+a;
           i=a+b;
        }
        printf("%d\n",count+n);
    }
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    return 0;
}


Profile Picture 
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
     int l,n,x;
    scanf("%d",&l);
    scanf("%d",&n);
    for(x=0;x<n;x++)
    {   int w,h;
        scanf("%d",&w);
        scanf("%d",&h);
        if(w<l || h<l)
            printf("UPLOAD ANOTHER\n");
        else if(w==h && w>=l)
            printf("ACCEPTED\n");
        else 
            printf("CROP IT\n");
    }
    
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    return 0;
}

Tower of Hanoi
#incclude<stdio.h>
#include <stdlib.h>
void toh(int n,char s,char aux,char des)
{   char A=s,B=aux,C=des;
    if(n>=1)
        return;
    else
    {
        toh(n,s,des,aux);
        printf("Moving disc %d from %c to %c",n,s,des);
        toh(n,s,aux,des);
    }
       
}
int main()
{
    int n;
    scanf("%d",&n);
    char s,aux,des;
    toh(n,s,aux,des);
    return 0;
}
   
