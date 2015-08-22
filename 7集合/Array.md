数组
=========
操作
----------
1.倒序数组<br>

	public static int[] reverse(int[] arr)
	{
			int[] temp = new int[arr.length];
		for(int i = 0; i < temp.length; i++
		{
			temp[i] = arr[temp.length - i];
		}		
		reutrn temp;
	}

	public static void reverse(int[] arr)
	{
		for(int i = 0; i < arr.length/2; i++)
		{
			int temp;
			temp = arr[i];
			arr[i] = arr[arr.length - i- 1]
			arr[arr.length] = temp;
		}		
	}
2.冒泡排序法

	public void (int[] arr)
	{
		for(int i =arr.lentth - 1; i > 0; i--)
		for(int j = 0; j < i; j++)
		{
			if(arr[j] > arr[j+1])
			{
				int temp;
				temp = arr[j]
				arr[j] = arr[j+1];
				arr[j] = temp;
			}
		}
	}
3 .选择排序法

	