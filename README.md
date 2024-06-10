# Binary-Search


#include <stdio.h>

int i=0, j=9,element;
int BinarySearch(int A[],int i,int j,int element){
  if (i<=j){
    int mid=(i+j)/2;
    if(A[mid]==element)
      return mid;
    else if (A[mid]>element)
      return BinarySearch(A,i,mid-1,element);
    else
      return BinarySearch(A,mid+1,j,element);
  }
  else
    return -1;
}

int main(void) {
  int mid;
  int A[] = {11,24,32,48,54,67,77,86,99,112};
  printf("Enter the element to be searched: ");
  scanf("%d",&element);
  mid = BinarySearch(A,i,j,element);
  if(mid==-1)
    printf("Element not found");
  else
    printf("Element found at index %d",mid);
  return 0;
}
