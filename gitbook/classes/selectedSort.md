选择性排序是数列排序的算法之一
线性搜索数列并找出最小值
将最小值替换为列中末梢的数字并进行排序
如果最小值已经在末端 则不执行任何操作
重复相同操作 直到所有数字都被排序

``` javascript

	var arr = [6,3,4,8,2,5,1,7,9];
	var result;

	function selectionSort(many){

		var arr = many.slice(),
		len = arr.length,minIndex,temp;

		for (var i = 0; i < len - 1; i++) {
			minIndex = i;
			for (var j = i + 1; j < len ; j++) {
			
				if(arr[j] < arr[minIndex])minIndex = j;
			};


			var tmp = arr[i];
			arr[i] = arr[minIndex];
			arr[minIndex] = tmp;
		};
		
		return arr;
	}
	result = selectionSort(arr);
	console.log(result,arr);

```