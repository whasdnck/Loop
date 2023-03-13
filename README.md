# Loop


### 반복문 이란 어떤 조건이 성립하는 동안 프로그램 명령문이나, 명령어의 집합을 반복 처리하는 구조를 반복 구조라고 부른다.
### 배열 a의 최댓값을 구하여 변환한다.
### for문을 사용하여 최댓값을 구한다.
### Max 함수를 사용하여 최댓값을 정한다.
### int[] height = new int[num]; 요솟수가 숫자인 배열을 생성한다.
### System.out.println("최댓값은 " + maxOf(height) + maxOf(height) + "입니다."); 를 사용하여 마지막 최댓값을 구할수있다.

# 반복문 코드
package sungil21102algo;
import java.util.Scanner;
public class Loop {
	// 배열 a의 최댓값을 구하여 변환
	static int maxOf(int[] a) {
		int max = a[0];
		for (int i =1; i < a.length; i++)
			if (a[i]>max)
					max = a[i];
		return max;
	}
	
	public static void main(String[] args) {
			Scanner stdIn = new Scanner(System.in);
			
		System.out.println("키의 최대값을 구합니다.");
		System.out.println("사람 수: ");
		int num = stdIn.nextInt();  // 배열의 요솟수를 입력받음
		
		int[] height = new int[num];	// 요솟수가 num인 배열을 생성
		
		for (int i =0; i<num; i++) {
			System.out.println("height[" + i +"] : ");
			height[i] = stdIn.nextInt();
		}
		
		System.out.println("최댓값은 " + maxOf(height) + maxOf(height) + "입니다.");	
	}
}
