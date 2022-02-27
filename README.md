# Maximum-frequency-of-a-word-in-a-string-if-the-input-is-well-defined
//This still needs optimisation
#include<stdio.h>
#include<string.h>
struct words
    {
        char string[100];
    }s1[10];
void main()
{
    
    printf("Enter a sentence: ");char a[200],greater[50];scanf("%[^\n]s",a);int i,j=0,len,big=0,count=0,itr=0;
    //printf("%s\n",a);
    len=strlen(a);char temp[len],k=0;
    printf("The entered string is: %s\n",a);
    //printf("Length of the string: %d\n",len);
    for(i=0;i<=len;i++)
    {
        if(a[i]==' '||a[i]=='\0')
        {
            strcpy(s1[k].string,temp);k++;
            //printf("%s\n",temp);
            memset(temp,0,strlen(temp));j=0;
            //strcpy(temp," ");
            //strcpy(s1[k].string," ");
            continue;
        }
        else
        {
        //printf("%c\n",a[i]);
        temp[j]=a[i];
        j++;
        }
    }
    
        for(i=0;i<k-1;i++)
        {
            for(j=i+1;j<k;j++)
            {
            if(strcmp(s1[i].string,s1[j].string)==0)
            count++;
            }
            //itr=count;
            if(count>big)
            {
                big=count;
                strcpy(greater,s1[i].string);
            }
            count=0;
        }
        for(i=0;i<k;i++)
        printf("%s\n",s1[i].string);
        printf("The word with high frequency is: %s\n",greater);
    
}
