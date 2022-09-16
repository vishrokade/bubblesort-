# bubblesort-
# write a bubblesort program in java


package vishal;

import java.util.Arrays;

public class bubblesort {

  public static void main(String[] args) {
		int[] arr= {2,3,5,9,8,2};
		int large = findlarger(arr);
		System.out.println("largest number in array is "+ large);
		sort(arr);
		System.out.println("\n the sorted array is\n");
		System.out.println(Arrays.toString(arr));
	}
  
  
	static int findlarger(int[] nums) {
		int large = 0;
		for(int i=0; i<nums.length; i++) {
			if (nums[i]>large)
			{
				large = nums[i];
			}
		}
		return large;
	}
	
	static void  sort(int[] nums) {
		for(int i=0; i<nums.length; i++) {
			
			for(int j=1; j<nums.length-i; j++) {
				
				if(nums[j]<nums[j-1]) {
					int temp = nums[j];
					nums[j]=nums[j-1];
					nums[j-1]=temp;
				}
			}
		}
	}
}
