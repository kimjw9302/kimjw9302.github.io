---
title: "Quick Sort(퀵정렬)"
date: 2019-07-15
categories:
  - Study
  - Sorting
  - JAVA
last_modified_at: 2019-03-09T12:45:25-05:00
---


### Quick Sorting(퀵정렬) ?
![퀵정렬이미지](/images/quick_img1.PNG) 
### 구현 코드(Java)
```javascript()
package Sort;

public class QuickSort {
	/** Quick Sort !! 퀵 정렬  ... 2019.07.09
	 * */
	public static void quickSort(int[] arr) {
		quickSort(arr,0,arr.length-1);
	}
	public static void quickSort(int[] arr, int start, int end ) {
		int p = partition(arr, start , end);
		if(start < p -1 ) {
			quickSort(arr,start,p-1);
		}
		if(p < end) {
			quickSort(arr,p,end);
		}
	}
	public static int partition(int[] arr, int start, int end){
		int pivot = start;
		int left = start;
		int right = end;
		while(left<=right) {
			while(arr[pivot] > arr[left]) {
				left++;
			}
			while(arr[pivot] < arr[right]) {
				right--;
			}
			if(left <= right) {
				swap(arr,left,right);
				left++;
				right--;
			}
		}
		return left;
	}

	public static void swap(int[] arr, int start, int end) {
		int tmp = arr[start];
		arr[start] = arr[end];
		arr[end] = tmp;
	}
	public static void main(String[] args) {
		int[] arr=  {3,9,4,7,5,0,1,6,8,2};
		quickSort(arr);
		for (int i = 0; i < arr.length; i++) {
			System.out.printf("%d\t",arr[i]);
		}
	}
}


```
![퀵정렬이미지](/images/quick_img2.PNG) 

```bash
퀵소트 / Quick Sorting
```
