---
title: "Counting Sort(카운팅정렬)"
date: 2019-07-1
categories:
  - Sorting
  - JAVA
last_modified_at: 2019-03-09T12:45:25-05:00
---


### Counting Sort(카운팅정렬)?

##### 항목들의 순서를 결정하기 위해 집합에 각 항목이
##### 몇개씩 있는지 세는 작업을 하여, 선형 시간에 정렬하는 효율적인 알고리즘

###### 
#### ![카운트1](/images/counting_img1.PNG)


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
#### ![버블2](/images/counting_img3.PNG)
```bash
Counting Sort / 카운팅정렬
```
