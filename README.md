#include<stdio.h>
void main()
{
    int i,j,k;
    int m1,n1,m2,n2;
    int a[10][10],b[10][10],c[10][10]=0;
    printf("enter the rows and columns of matrix a:\n");
    scanf("%d %d",&m1,&n1);
    printf("enter the rows and column of matrix B:\n");
    scanf("%d %d",&m2,&n2);
    if(m1!=n2){
        printf("the mtrix multiplication is not possible");
        return ;
    }
    printf("enter the elements of matrix a:");
    for(i=0;i<m1;i++)
        {
            for(j=0;j<n1;j++)
                {
                    scanf("%d",&a[i][j]);
                }

        }
    printf("enter the elements of matrix b:\n");
    for(i=0;i<m2;i++)
        {
            for(j=0;j<n2;j++)
                {
                    scanf("%d",&b[i][j]);
                }
        }
    for(i=0;i<m1;i++)
        {
            for(j=0;j<n2;j++)
                {
                    for(k=0;k<n1;k++)
                        {
                            c[i][j]+=a[i][k]*b[k][j];
                        }
                }
        }
    
    printf("the resultant matrix is :\n");
    for(i=0;i<m1;i++)
        {
            for(j=0;j<n2;j++)
                {
                    printf("%d",c[i][j]);
                }
                printf("\n");
        }
}
