---
title: "Bubble Sort(버블정렬)!"
date: 2019-07-17
categories:
  - Sorting
  - JAVA
last_modified_at: 2019-03-09T12:45:25-05:00
---


### Bubble Sort(버블정렬)?

##### 이중포문 구현,
##### 바깥 포문은 i = N-1 -> 0 포문을 돌리고,
##### 안쪽 포문은 0부터  i 번만큼 돌립니다.
##### 결국 회차별 가장 큰 값은 뒤로 가지기 때문에
##### 반복 횟수를 줄일 수 있는 코드
##### 배열[J],배열[J+1]번를 잡고 비교하면서 swap.

###### 최선 O(n) - 최악 O(n^2)
#### ![버블1](/images/bubble_img1.PNG)

#### ![버블2](/images/bubble_img2.PNG)

##### < 자바 코드 >
```javascript()

import java.util.Arrays;

public class Bubble {
	int[] arr;
	Bubble(int [] arr){
		this.arr = arr;
		
	}
	public void swap(int a,int b) {
		int temp = arr[a];
		arr[a] = arr[b];
		arr[b] = temp;
	}
	public void sort(){
			
		for(int i = arr.length-1; i >= 0;i--) {
			System.out.println(arr.length-i+ "회차");
			for(int j = 0 ; j < i ;j++) {
				if(arr[j]>arr[j+1]) {
					this.swap(j,j+1);
					System.out.println(Arrays.toString(arr));
				}
				
			}
		}		
	}
	public static void main(String[] args) {
		
		int[] arr = {8,5,6,2,4};
		Bubble b= new Bubble(arr);
		b.sort();
		System.out.println("정렬완료!");
		System.out.println(Arrays.toString(arr));
	} 
}
##### < 결과창 >
#### ![버블2](/images/bubble_img3.PNG)
```
```bash
한국관광공사
```
