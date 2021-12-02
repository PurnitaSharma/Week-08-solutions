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
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>
void towerofhanoi(int n,char A,char C,char B)
{
    if(n<=1)
        printf("Moving ring %d from %c to %c\n\n",n,A,C);
    else
    {
        towerofhanoi(n-1,A,B,C);
        printf("Moving ring %d from %c to %c\n\n",n,A,C);
        towerofhanoi(n-1,B,C,A);
    }
}
int main() {
    int n;
    scanf("%d",&n);
    towerofhanoi(n,'A','C','B');
     
    /* Enter your code here. Read input from STDIN. Print output to STDOUT */    
    return 0;
}

   
