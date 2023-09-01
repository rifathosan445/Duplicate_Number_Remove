# Duplicate_Number_Remove
Write a C program that reads a string as an input from the user where multiple numbers are separated by commas. Then, make a array of numbers from the input string and print the array. Finally, remove multiple occurrences of any numbers from the input array and print the modified array without duplicate values.


    #include <stdio.h>
    int main()
    {
      char s1[]="RifatRasan";
      int len=strlen(s1);
      int a[len+1],i,count=0,j,k;
      for(i=0;s1[i]!='\0';i++)
      {
            a[i]=s1[i] ;
            count++;
      }
      for(i=0;i<count;i++)
      {
             for(j=i+1;j<count;j++)
             {
                    if(a[i]==a[j])
                    {
                           for(k=j;k<count;k++)
                           {
                                  a[k]=a[k+1];
                                  count--;
                                  j--;
                           }
                    }
             }
      }
      for(i=0;i<count;i++)
      {
         printf("%d,",a[i])  ;
      }
    
    }
    
    
