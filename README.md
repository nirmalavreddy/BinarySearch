# BinarySearch

public class BinarySearch {

public static void main(String[] args) 
{
	int[] a = {2,5,7,9,12,14};
	int key = 5;
	int low=0;
	int high = a.length-1;
	int mid = (low+high)/2;
	while(low <= high)
	{
		//if mid element and key are equal
		if(a[mid] == key)
		{
			System.out.println("element is at "+mid+" index position");
			break;
		}
		
		//if mid element is greater than key
		else if(a[mid]<key)
		{
			low =mid+1;
		}
		
		//if mid element is lesser than key
		else
		{
			high=mid-1;
		}
		mid = (low+high)/2;
	}
	
	//searched completely but could not find the element
	if(low > high)	
	{
		System.out.println("element not found");
	}
}
}
