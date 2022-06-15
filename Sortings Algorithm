Kiet Nguyen
//CECS 328 Sec 01; Summer 2022
//6/10/22

import java.util.Arrays;
import java.util.Random;

public class Main {

	private static void reverse(int[] array) {
		// Length of the array
        int n = array.length;
  
        // Swapping the first half elements with last half
        
        for (int i = 0; i < n / 2; i++) {
  
            // Storing the first half elements temporarily
            int temp = array[i];
  
            // Assigning the first half to the last half
            array[i] = array[n - i - 1];
  
            // Assigning the last half to the first half
            array[n - i - 1] = temp;
        }
	}
	
	// Print class to solution check the sorting
	private static void printArray(int[] array) {
		String a = Arrays.toString(array);
		System.out.println(a );
	}
	
	// Swap inside array class
  void elementSwap(int[] array, int element1, int element2){
    int hold = array[element1];
    array[element1] = array[element2];
    array[element2] = hold;
  }
  
	// Set up Insertion Sort class
	void insertionsort(int array[]) {
		int n = array.length;
        for (int i = 1; i < n; i++) {
            int current = array[i];
            int j = i - 1;
 
         
            while (j >= 0 && array[j] < current) {
                array[j + 1] = array[j];
                j = j - 1;
            }
         array[j + 1] = current;
        }
	}
	
	// Display Insertion Sort Run Time
	public static double displayInsSort (int arr[]) {
		 double start = System.nanoTime();
		 Main test = new Main();
		 test.insertionsort(arr);
		 double duration = (System.nanoTime()- start)/ 1000000;
		 return duration;
	}

  // Set up Bubble Sort class
	void bubblesort(int array[]) {
		boolean swap = true;
		
		while(swap) {
			swap = false;
			for (int i = 0; i < array.length - 1; i++) {
			if (array[i] < array[i+1]) {
				swap = true;		
				int temp = array[i];
				array[i] = array[i+1];
				array[i+1] = temp;
			  }
			}
		}
	}
	// Display Bubble Sort Run Time
		public static double displayBubSort (int arr[]) {
			 double start1 = System.nanoTime();
			 Main test1 = new Main();
			 test1.bubblesort(arr);
			 double duration1 = (System.nanoTime()- start1)/ 1000000;
			 return duration1;
		}
  
  // Partition class
  int Partition(int[] array,int first, int last){
    int pivot = array[last];
    int i = first - 1;
    for (int j = first; j <= last; j++){
      if  (array[j] > pivot){
        i++;
        elementSwap(array, i, j);
      } 
    }
    elementSwap(array, i+1, last);
    return (i + 1);
  }
  
  //QuickSort class
  void quicksort(int[] array, int first, int last){
    if (first < last){
      int parIndex = Partition(array, first, last);
      quicksort(array, first, parIndex - 1);
      quicksort(array, parIndex + 1, last);
    }
  }
  //Dipslay Quick Sort time
  public static double displayQuickSort (int arr[]) {
		 double start = System.nanoTime();
		 Main test = new Main();
     int n = arr.length;
		 test.quicksort(arr, 0, n - 1);
		 double duration = (System.nanoTime()- start)/ 1000000;
		 return duration;
	}

  //merge class
  static void merge(int arr[], int first, int middle, int last){
    //Get subarray sizes
    int size1 = middle - first + 1;
    int size2 = last - middle;

    //Making the arrays to be merged
    int [] LeftA = new int[size1];
    int [] RightA = new int[size2];
    
    for (int i = 0; i < size1; i++){
      LeftA[i] = arr[first + i];
    }
    for (int j = 0; j < size2; j++){
      RightA[j] = arr[middle + 1 + j];
    }
    
    //Merging the arrays 
    int i = 0;
    int j = 0;
    int k = first;
    while (i < size1 && j < size2){
      if (LeftA[i] >= RightA[j]){
        arr[k] = LeftA[i];
        i++;
      }
      else{
        arr[k] = RightA[j];
        j++;
        }
      k++;
    }
    
    while (i < size1){
      arr[k] = LeftA[i];
      i++;
      k++;
    }
    while (j < size2){
      arr[k] = RightA[j];
      j++;
      k++;
    }
  }
  
  //MergeSort class
  void mergesort(int[] array, int first, int last){
    if (first < last){
      int middle = (int) Math.floor((first + last)/2);
      mergesort(array, first, middle);
      mergesort(array, middle + 1, last);
      merge(array, first, middle, last);
    }
  }

  //Display Merge Sort time
  public static double displayMergeSort (int arr[]) {
		 double start = System.nanoTime();
		 Main test = new Main();
     int n = arr.length;
		 test.mergesort(arr, 0, n - 1);
		 double duration = (System.nanoTime()- start)/ 1000000;
		 return duration;
	}

  
	// Create an Array with 1000 ascending elements
	static int[] ascendingArr() {
		Random r = new Random();
		int [] ascendingArr = new int [1000];
		 for (int i=0; i< ascendingArr.length; i++) {
			 ascendingArr[i] = r.nextInt(-1000,1000); 
			 Arrays.sort(ascendingArr);
		 }
		 return ascendingArr;
	}
	
	// Create an Array with 1000 descending elements
	static int[] decArr() {
		Random r = new Random();
		int [] decArr = new int[1000];
		 for (int i=0; i< decArr.length; i++) {
			 decArr[i] = r.nextInt(-1000,1000); 
			 Arrays.sort(decArr);
			 reverse(decArr);
		 }
		return decArr;
	}
	
	// Create an Array with 1000 random elements
	static int[] ranArr1k() {
		Random r = new Random();
		int [] ranArr1k = new int [1000];
		 for (int i=0; i< ranArr1k.length; i++) {
			 ranArr1k[i] = r.nextInt(-1000,1000); 
		 }
		return ranArr1k;
	}
	
	// Create an Array with 10000 random elements	 
	static int[] ranArr10k() {
		Random r = new Random();
		int [] ranArr10k = new int [10000];
		 for (int i=0; i< ranArr10k.length; i++) {
			 ranArr10k[i] = r.nextInt(-10000,10000);  
		 }
		return ranArr10k;
	}
	public static void main(String[] args) {
		 // Insertion Sort with 1000 descending elements
     int[] arr = decArr();
     double a = displayInsSort(arr);
     System.out.println("Insertion Sort with 1000 descending elements: " + a + " ms");
		 
		//Insertion Sort with 1000 ascending elements
		 int[] arr1 = ascendingArr();
		 double a1 = displayInsSort(arr1);
		 System.out.println("Insertion Sort with 1000 ascending elements: " 
				 + a1 + " ms");
		 
		//Insertion Sort with 1000 random elements
		 int[] arr2 = ranArr1k();
		 double a2 = displayInsSort(arr2);
		 System.out.println("Insertion Sort with 1000 random elements: " 
				 + a2 + " ms");
		 
		//Insertion Sort with 10000 random elements
		 int[] arr3 = ranArr10k();
		 double a3 = displayInsSort(arr3);
		 System.out.println("Insertion Sort with 10000 random elements: " 
				 + a3 + " ms");
				 
		//Bubble Sort with 1000 descending elements
		 int[] arr4 = decArr();
		 double a4 = displayBubSort(arr4);
		 System.out.println("Bubble Sort with 1000 descending elements: " 
				 + a4 + " ms");
		 
		//Bubble Sort with 1000 ascending elements
		 int[] arr5 = ascendingArr();
		 double a5 = displayBubSort(arr5);
		 System.out.println("Bubble Sort with 1000 ascending elements: " 
				 + a5 + " ms");
		 
		//Bubble Sort with 1000 random elements
		 int[] arr6 = ranArr1k();
		 double a6 = displayBubSort(arr6);
		 System.out.println("Bubble Sort with 1000 random elements: " 
				 + a6 + " ms");
		 
		//Bubble Sort with 10000 random elements
		 int[] arr7 = ranArr10k();
		 double a7 = displayBubSort(arr7);
		 System.out.println("Bubble Sort with 10000 random elements: " 
				 + a7 + " ms");

    //Quick sort with 1000 descending elements
    int [] Qarr1 = decArr();
    double q1 = displayQuickSort(Qarr1);
    System.out.println("Quick Sort with 1000 descending elements: " + q1 + " ms");

    //Quick sort with 1000 ascending elements
    int [] Qarr2 = ascendingArr();
    double q2 = displayQuickSort(Qarr2);
    System.out.println("Quick Sort with 1000 ascending elements: " + q2 + " ms");

    //Quick sort with 1000 random elements
    int [] Qarr3 = ranArr1k();
    double q3 = displayQuickSort(Qarr3);
    System.out.println("Quick Sort with 1000 random elements: " + q3 + " ms");

    //Quick sort with 10000 random elements
    int [] Qarr4 = ranArr10k();
    double q4 = displayMergeSort(Qarr4);
    System.out.println("Quick Sort with 10000 random elements: " + q4 + " ms");

    //Merge sort with 1000 descending elements
    int [] Marr1 = decArr();
    double m1 = displayQuickSort(Marr1);
    System.out.println("Merge Sort with 1000 descending elements: " + m1 + " ms");

    //Quick sort with 1000 ascending elements
    int [] Marr2 = ascendingArr();
    double m2 = displayQuickSort(Marr2);
    System.out.println("Merge Sort with 1000 ascending elements: " + m2 + " ms");

    //Quick sort with 1000 random elements
    int [] Marr3 = ranArr1k();
    double m3 = displayQuickSort(Marr3);
    System.out.println("Merge Sort with 1000 random elements: " + m3 + " ms");

    //Quick sort with 10000 random elements
    int [] Marr4 = ranArr10k();
    double m4 = displayQuickSort(Marr4);
    System.out.println("Merge Sort with 10000 random elements: " + m4 + " ms");
  
    
     
	}
}

