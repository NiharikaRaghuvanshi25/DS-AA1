#include <stdio.h>
void swap(int *x, int *y) {
    int temp = *x;
    *x = *y;
    *y=temp;
  }
  void heapify(int arr[], int n, int i) {
    int root = i;
    int left = 2 * i ;
    int right = 2 * i + 1;
  
    if (left < n && arr[left] > arr[root])
      root=left;
  
    if (right < n && arr[right] > arr[root])
      root=right;
  if (root!= i) {
      swap(&arr[i], &arr[root]);
      heapify(arr,root,n);
    }
  }
  void heapSort(int arr[], int n) {
    for (int i = n / 2 - 1; i >= 0; i--)
      heapify(arr, n, i);
  for (int i = n - 1; i >= 0; i--) {
      swap(&arr[0], &arr[i]);
  heapify(arr, i, 0);
    }
  }
  void printArray(int arr[], int n) {
    for (int i = 0; i < n; ++i)
      printf("%d ", arr[i]);
    printf("\n");
  }
   int main() {
    int arr[] = {10,7,91,299,68,40};
    int n = sizeof(arr) / sizeof(arr[0]);
  
    heapSort(arr, n);
  
    printf("Sorted List is \n");
    printArray(arr, n);
  }
