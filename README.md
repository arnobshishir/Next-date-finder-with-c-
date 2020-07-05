// Next-date-finder-with-c-
//intput date/month/year output next date
#include<stdio.h>
int main(void)
{
    int d,m,y;
    printf("Enter Date :");
    scanf("%d",&d);
    printf("Enter Month :");
    scanf("%d",&m);
    printf("Enter year :");
    scanf("%d",&y);

    if(m==12)
    {
        if(d==31)
        {
            m=1;
            d=1;
            y++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else if(d<31 && d>=1)
        {
            d++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else
        {
            printf("\n invalid date!");
        }
    }
    else if(m==4 || m==6 || m== 9 || m== 11)
    {
        if(d=30)
        {
            d=1;
            m++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else if(d<30 && d>=1)
        {
            d++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else
        {
            printf("\n invalid date !\n");
        }
    }
    else if(m==2)
    {
        if((y%400==0) || (y%4==0 && y%100!=0))
        {
            if(d==29)
            {
                d=1;
                m=3;
                printf("The next date is : %d-%d-%d\n",d,m,y);
            }
            else if(d<29 && d>=1)
            {
                d++;
                printf("The next date is : %d-%d-%d\n",d,m,y);
            }
            else
                printf("\n Invalid date!");
        }
        else
        {
            if(d==28)
            {
                d=1;
                m=3;
                printf("The next date is : %d-%d-%d\n",d,m,y);
            }
            else if(d<28 && d>=1)
            {
                d++;
                printf("The next date is : %d-%d-%d\n",d,m,y);
            }
            else
                printf("\n invalid date");
        }

    }
    else if(m==1|| m==3 ||m==5 ||m==7|| m==8|| m==10)
    {
        if(d==31)
        {
            d=1;
            m++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else if(d<31 && d>=1)
        {
            d++;
            printf("The next date is : %d-%d-%d\n",d,m,y);
        }
        else
        {
            printf("\n Invalid date !");
        }
    }
    else
    {
        printf("\n Invalid date input");
    }

}
