#include <stdio.h>

int main() {
  double num1, num2;
  char operator;
  int s;
  
  again:
  printf("Enter first number: ");
  scanf("%lf", &num1);
  printf("Enter second number: ");
  scanf("%lf", &num2);
  printf("Enter an operator (+, -, *, /): ");
  scanf(" %c", &operator);
  
  switch (operator) {
    case '+':
      printf("%.1lf + %.1lf = %.1lf", num1, num2, num1 + num2);
      printf("\n");
      break;
    case '-':
      printf("%.1lf - %.1lf = %.1lf", num1, num2, num1 - num2);
      printf("\n");
      break;
    case '*':
      printf("%.1lf * %.1lf = %.1lf", num1, num2, num1 * num2);
      printf("\n");
      break;
    case '/':
      printf("%.1lf / %.1lf = %.1lf", num1, num2, num1 / num2);
      printf("\n");
      break;
    default:
      printf("Error: Invalid operator\n");
      goto again;
  }
    again2:
    printf("enter 1 to continue : \n");
    printf("enter 2 to quit : \n");
    scanf("%d", &s);
    switch (s)
    {
    case 1:
      goto again ;
      printf("\n");
    break;
    case 2:
    break; 
    default:
      printf("Error: Invalid choice\n");
      goto again2;
    break;
  }

  return 0;
}
