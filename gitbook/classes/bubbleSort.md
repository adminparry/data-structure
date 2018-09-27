冒泡排序是数列排序的算法之一
将两个相邻的数进行比较
按照你想要的序列进行交换
逐一比较两个数字
重复相同操作 直到所有数字都被排序

``` javascript

	var arr = [5,9,3,1,2,8,4,7,6];
	var result;

	function bubbleSort(many){

		var arr = many.slice();

		for (var i = 0; i < arr.length - 1; i++) {

			for (var j = 0; j < arr.length - 1 - i; j++) {
			
				if(arr[j] < arr[j + 1])continue;
			
				var tmp = arr[j];
				arr[j] = arr[j + 1];
				arr[j + 1] = tmp;

			};
		};
		
		return arr;
	}
	result = bubbleSort(arr);
	console.log(result,arr);

```