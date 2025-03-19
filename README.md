# C-Programing

---

## **1. If-Else Assignments**  

### **Q1: Check whether a number is even or odd**  
```c
#include <stdio.h>

int main() {
    int num;

    // Input from user
    printf("Enter a number: ");
    scanf("%d", &num);

    // Checking if the number is even or odd
    if (num % 2 == 0) {
        printf("%d is Even\n", num);
    } else {
        printf("%d is Odd\n", num);
    }

    return 0;
}
```
#### **Explanation:**
- We take input from the user.
- If a number is divisible by 2 (`num % 2 == 0`), it's even; otherwise, it's odd.

---

### **Q2: Check whether a number is positive, negative, or zero**
```c
#include <stdio.h>

int main() {
    int num;

    printf("Enter a number: ");
    scanf("%d", &num);

    if (num > 0) {
        printf("The number is positive\n");
    } else if (num < 0) {
        printf("The number is negative\n");
    } else {
        printf("The number is zero\n");
    }

    return 0;
}
```
#### **Explanation:**
- We check if `num > 0`, `num < 0`, or `num == 0` and print the appropriate message.

---

### **Q3: Find the largest of two numbers**
```c
#include <stdio.h>

int main() {
    int a, b;
    
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);

    if (a > b) {
        printf("%d is greater\n", a);
    } else if (b > a) {
        printf("%d is greater\n", b);
    } else {
        printf("Both numbers are equal\n");
    }

    return 0;
}
```

---

## **2. Loops Assignments**  

### **Q4: Print numbers from 1 to N using a for loop**
```c
#include <stdio.h>

int main() {
    int N, i;

    printf("Enter the value of N: ");
    scanf("%d", &N);

    // Loop from 1 to N
    for (i = 1; i <= N; i++) {
        printf("%d ", i);
    }
    
    return 0;
}
```
---

### **Q5: Print even numbers from 1 to N using a while loop**
```c
#include <stdio.h>

int main() {
    int N, i = 2; // Start from the first even number

    printf("Enter the value of N: ");
    scanf("%d", &N);

    while (i <= N) {
        printf("%d ", i);
        i += 2; // Increment by 2 to get the next even number
    }
    
    return 0;
}
```
---

### **Q6: Reverse a number**
```c
#include <stdio.h>

int main() {
    int num, reversed = 0, remainder;

    printf("Enter a number: ");
    scanf("%d", &num);

    while (num != 0) {
        remainder = num % 10;  // Extract the last digit
        reversed = reversed * 10 + remainder; // Append the digit
        num /= 10; // Remove the last digit
    }

    printf("Reversed Number: %d\n", reversed);

    return 0;
}
```
---

## **3. Pattern Printing Assignments**  

### **Q7: Print a right-angled triangle pattern**
```
*
* *
* * *
* * * *
```
```c
#include <stdio.h>

int main() {
    int i, j, rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (i = 1; i <= rows; i++) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

---

### **Q8: Print an inverted triangle**
```
*****
****
***
**
*
```
```c
#include <stdio.h>

int main() {
    int i, j, rows;

    printf("Enter the number of rows: ");
    scanf("%d", &rows);

    for (i = rows; i >= 1; i--) {
        for (j = 1; j <= i; j++) {
            printf("* ");
        }
        printf("\n");
    }

    return 0;
}
```

---

## **4. Number Series Assignments**  

### **Q9: Fibonacci series up to N terms**
```c
#include <stdio.h>

int main() {
    int n, t1 = 0, t2 = 1, nextTerm;

    printf("Enter the number of terms: ");
    scanf("%d", &n);

    printf("Fibonacci Series: %d, %d", t1, t2);

    for (int i = 3; i <= n; i++) {
        nextTerm = t1 + t2;
        printf(", %d", nextTerm);
        t1 = t2;
        t2 = nextTerm;
    }

    return 0;
}
```
---

### **Q10: Check if a number is prime**
```c
#include <stdio.h>

int main() {
    int num, i, flag = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    if (num < 2) {
        printf("Not a prime number\n");
        return 0;
    }

    for (i = 2; i <= num / 2; i++) {
        if (num % i == 0) {
            flag = 1; // Number is not prime
            break;
        }
    }

    if (flag == 0)
        printf("%d is a prime number\n", num);
    else
        printf("%d is not a prime number\n", num);

    return 0;
}
```
---

### **Q11: Sum of digits of a number**
```c
#include <stdio.h>

int main() {
    int num, sum = 0, digit;

    printf("Enter a number: ");
    scanf("%d", &num);

    while (num != 0) {
        digit = num % 10; // Extract the last digit
        sum += digit; // Add digit to sum
        num /= 10; // Remove the last digit
    }

    printf("Sum of digits: %d\n", sum);

    return 0;
}
```
---

