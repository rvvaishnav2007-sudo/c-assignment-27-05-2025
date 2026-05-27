# c-assignment-27-05-2025
## NAME : Vaishnav V
## REG NO :212224060291
1. 1. Write a program to read a string and count the number of vowels using a separate function.
```
#include <stdio.h>

int countVowels(char str[])
{
    int i = 0, count = 0;

    while(str[i] != '\0')
    {
        char ch = str[i];

        if(ch=='a' || ch=='e' || ch=='i' || ch=='o' || ch=='u' ||
           ch=='A' || ch=='E' || ch=='I' || ch=='O' || ch=='U')
        {
            count++;
        }

        i++;
    }

    return count;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of vowels = %d", countVowels(str));

    return 0;
}
}
```
##  output
<img width="1909" height="1138" alt="image" src="https://github.com/user-attachments/assets/6cf9b988-5b7b-4211-9d60-d0ea676f1dee" />



2.2. Write a function to reverse a string without using library functions like strrev().
```
#include <stdio.h>

void reverseString(char str[])
{
    int i = 0, len = 0;
    char temp;

    while(str[len] != '\0')
    {
        len++;
    }

    len--;

    while(i < len)
    {
        temp = str[i];
        str[i] = str[len];
        str[len] = temp;

        i++;
        len--;
    }
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    reverseString(str);

    printf("Reversed string = %s", str);

    return 0;
}
```
## output
<img width="1890" height="1068" alt="image" src="https://github.com/user-attachments/assets/a02c67cd-3e37-42f5-b9bc-c9ee81228972" />


3.3. Write a program to check whether a given string is palindrome or not using functions.
```
#include <stdio.h>

int isPalindrome(char str[])
{
    int i = 0, len = 0;

    while(str[len] != '\0')
    {
        len++;
    }

    len--;

    while(i < len)
    {
        if(str[i] != str[len])
        {
            return 0;
        }

        i++;
        len--;
    }

    return 1;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    if(isPalindrome(str))
        printf("Palindrome");
    else
        printf("Not Palindrome");

    return 0;
}

```
## output

<img width="1906" height="1097" alt="image" src="https://github.com/user-attachments/assets/ffd1e1d2-86ff-4f22-b6b3-f11ee7f2fec7" />


4. 4. Write a function to calculate the length of a string manually.
```
#include <stdio.h>

int stringLength(char str[])
{
    int len = 0;

    while(str[len] != '\0')
    {
        len++;
    }

    return len;
}

int main()
{
    char str[100];

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Length of string = %d", stringLength(str));

    return 0;
}

```
## output

<img width="1706" height="1079" alt="image" src="https://github.com/user-attachments/assets/e76e38e0-482c-4c6f-98b8-69677b230811" />


5. Write a function to count the number of words in a sentence.
```
#include <stdio.h>

int countWords(char str[])
{
    int i = 0, count = 1;

    while(str[i] != '\0')
    {
        if(str[i] == ' ')
        {
            count++;
        }

        i++;
    }

    return count;
}

int main()
{
    char str[200];

    printf("Enter a sentence: ");
    fgets(str, sizeof(str), stdin);

    printf("Number of words = %d", countWords(str));

    return 0;
}
```
## output
<img width="1701" height="1091" alt="image" src="https://github.com/user-attachments/assets/0e5b01f1-8be4-49b8-873a-ce900cbd6c83" />
