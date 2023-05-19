# Brute force password cracking code 
  __using C language__

``` bash
#include <stdio.h>
#include <string.h>
int main()
{
    char password[11] = "vatiza1920";
    int len = strlen(password);
    int valid = 1;
    if (len != 6 && len != 10)
    {
        valid = 0;
    }
    for (int i = 0; i < len; i++)
    {
        char c = password[i];
        if (!((c >= '0' && c <= '9') || (c >= 'a' && c <= 'z') ||
              c == '&' || c == '*' || c == '#'))
        {
            valid = 0;
            break;
        }
    }
    if (valid)
    {
        printf("The password is valid.\n");
    }
    else
    {
        printf("The password is invalid.\n");
    }
    return 0;
}
```
