---
title: "Counting Sort(카운팅정렬)"
date: 2019-07-1
categories:
  - Sorting
  - JAVA
last_modified_at: 2019-03-09T12:45:25-05:00
---


### Counting Sort(카운팅정렬)?

##### 이중포문 구현,
##### 바깥 포문은 i = N-1 -> 0 포문을 돌리고,
##### 안쪽 포문은 0부터  i 번만큼 돌립니다.
##### 결국 회차별 가장 큰 값은 뒤로 가지기 때문에
##### 반복 횟수를 줄일 수 있는 코드
##### 

###### 
#### ![카운트1](/images/counting_img1.PNG)

#### ![카운트2](/images/counting_img2.PNG)

##### < 자바 코드 >
```javascript()

import java.util.Arrays;
import java.util.Random;
/*
 *  카운팅 정렬
 *  */
public class CountingSort {
	public static void main(String[] args) {
		Random rand = new Random();
		int[] numbers = new int[10];
		int max = 0;
		for (int i = 0; i < 10; i++) {
			numbers[i] = rand.nextInt(100) + 1;
			if(max < numbers[i]) {//배열 내 최대값 찾기.
				max = numbers[i];
			}
		}
		int[] sorted = new int[numbers.length]; // 정렬된 배열넣기.
		System.out.println("배열 내 최대값 : "+max);
		int[] counts = new int[max+1];
		//카운트 세기!	
		for(int i = 0 ; i < numbers.length; i++) {		
			counts[numbers[i]]++;
		}
		//카운트 누적 시키기!
		for(int i = 1 ; i < counts.length;i++) {		
				counts[i] = counts[i]+counts[i-1];			
		}
		System.out.println(Arrays.toString(counts));
		//배정하기
		for(int i = 0 ; i < numbers.length; i++) {
				counts[numbers[i]]--;
				sorted[counts[numbers[i]]] = numbers[i];						
		}
		
		System.out.println(Arrays.toString(sorted));
		
		
		System.out.println(Arrays.toString(numbers));
	}
}


```
##### < 결과창 >
#### ![버블2](/images/bubble_img3.PNG)
```bash
Counting Sort / 카운팅정렬
```
