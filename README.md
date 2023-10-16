# ArrayShuffle
package Assg;

import java.util.ArrayList;
import java.util.Arrays;
//import java.util.Collections;
import java.util.List;
import java.util.Random;

public class ArrayShuffle {
	public static void main(String[] args) {
		int[] array = { 1, 2, 3, 4, 5, 6, 7 };
		shuffleArray(array);

		for (int num : array) {
			System.out.print(num + " ");
		}
	}
	public static void shuffleArray(int[] array) {
		int n = array.length;
		Random rand = new Random();

		for (int i = n - 1; i > 0; i--) {	
			int j = rand.nextInt(i + 1);
			int temp = array[i];
			array[i] = array[j];
			array[j] = temp;
		}
	}
}
