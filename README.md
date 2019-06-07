# 1D-Array
#include <stdio.h>
#include <string.h>
#include <math.h>
#include <stdlib.h>

int main() {
  int *ptr;  // declaration of integer pointer
  int limit; // to store array limit
  int i;     // loop counter
  int sum=0;   // to store sum of all elements

  scanf("%d", &limit);

  // declare memory dynamically
  ptr = (int *)malloc(limit * sizeof(int));

  // read array elements
  for (i = 0; i < limit; i++) {

    scanf("%d", (ptr + i));
  }

 
 

  // calculate sum of all elements
 
  for (i = 0; i < limit; i++) {
    sum += *(ptr + i);
  }
  printf("%d\n", sum);

  // free memory
  free(ptr); 

  return 0;
}

