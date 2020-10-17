#include <stdio.h>
void insertionSort(int arr[], int n) 
{ 
    int i, p, j; 
    for (i = 1; i < n; i++) { 
        p = arr[i]; 
        j = i - 1; 
  
        while (j >= 0 && arr[j] > p) { 
            arr[j + 1] = arr[j]; 
            j = j - 1; 
        } 
        arr[j + 1] = p; 
    } 
} 
  

      
void merge(int arr[], int l, int m, int r) 
{ 
    int i, j, k; 
    int a = m - l + 1; 
    int b = r - m; 
  
    
    int N[a], M[b]; 
  
    
    for (i = 0; i < a; i++) 
        N[i] = arr[l + i]; 
    for (j = 0; j < b; j++) 
        M[j] = arr[m + 1 + j]; 
  
   
    i = 0; 
    j = 0; 
    k = l;
    while (i < a && j < b) { 
        if (N[i] <= M[j]) { 
            arr[k] = N[i]; 
            i++; 
        } 
        else { 
            arr[k] = M[j]; 
            j++; 
        } 
        k++; 
    } 
  
    while (i < a) { 
        arr[k] = N[i]; 
        i++; 
        k++; 
    } 
  
    while (j < b) { 
        arr[k] = M[j]; 
        j++; 
        k++; 
    } 
} 
  


void mergeSort(int arr[], int l, int r) 
{ 
    if (l < r) { 
        
        int m = l + (r - l) / 2; 
  
        
        mergeSort(arr, l, m); 
        mergeSort(arr, m + 1, r); 
  
        merge(arr, l, m, r); 
    } 
} 

void swap(int* a, int* b) 
{ 
    int t = *a; 
    *a = *b; 
    *b = t; 
} 
  

int partition(int arr[], int down, int up) 
{ 
    int pivot = arr[up];     
    int i = (down - 1);   
  
    for (int j = down; j <= up- 1; j++) 
    { 
         
        if (arr[j] < pivot) 
        { 
            i++;     
            swap(&arr[i], &arr[j]); 
        } 
    } 
    swap(&arr[i + 1], &arr[up]); 
    return (i + 1); 
} 
  

       
           
void quickSort(int arr[], int down, int up) 
{ 
    if (down < up) 
    { 
        
        int pi = partition(arr, down, up); 
  
        
        quickSort(arr, down, pi - 1); 
        quickSort(arr, pi + 1, up); 
    } 
} 
 void heapify(int arr[], int n, int i) {
    
    int largest = i;
    int left = 2 * i + 1;
    int right = 2 * i + 2;
  
    if (left < n && arr[left] > arr[largest])
      largest = left;
  
    if (right < n && arr[right] > arr[largest])
      largest = right;
  
    
    if (largest != i) {
      swap(&arr[i], &arr[largest]);
      heapify(arr, n, largest);
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

void printArray(int A[], int size) 
{ 
    int i; 
    for (i = 0; i < size; i++) 
        printf("%d ", A[i]); 
    printf("\n"); 
} 
  
  
int main() 
{ 
 
    int n;
    printf("Enter the size of the array : ");
    scanf("%d",&n);
    printf("Enter the elements of the array : \n");
    int arr[n];
    for(int i=0;i<n;i++){
        scanf("%d",&arr[i]);
    }
    printf("The sorted array after applying insertion sort is : ");
    insertionSort(arr, n); 
    printArray(arr, n); 
    printf("The sorted array after applying merge sort is : ");
    mergeSort(arr, 0, n - 1); 
    printArray(arr, n); 
    printf("The sorted array after applying quick sort is : ");
    quickSort(arr, 0, n-1);
    printArray(arr, n);
    printf("The sorted array after applying heap sort is : ");
    heapSort(arr, n);
    printArray(arr, n);
    
    return 0; 
} 
