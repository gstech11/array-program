# array-program

/*P2.2 Program to find the largest and smallest number in an array*/
#include<stdio.h>
main( )
{
	int i,arr[10]={ 2, 5, 4, 1, 8, 9, 11, 6, 3, 7 };
	int small, large;
	small = large = arr[0];
	for(i=1; i<10; i++)
	{
		if(arr[i] < small)
			small = arr[i];
		if(arr[i] > large )
			large = arr[i];
	}
	printf("Smallest = %d, Largest = %d\n", small, large);
}



/* P2.4 Program to pass array elements to a function */
#include<stdio.h>
void check(int num);
main( )
{
	int arr[10], i;
	printf("Enter the array elements : ");
	for(i=0; i<10; i++)
	{
		scanf("%d", &arr[i]);
		check(arr[i]);
	}
}
void check(int num)
{
	if(num%2==0)
		printf("%d is even\n", num);
	else
       	printf("%d is odd\n", num);
}
