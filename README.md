array sorter
no sort()

ex.
input: array[9, 2, 7, 12]
output: array[2, 7, 9, 12]

array length unknown.


const sortArray = (arr) => {
	const length = arr.length;
	if( length == 1 || isNaN(arr))
    	return;
    for(let i=0; i >= length; i++)
    	if(arr[i] > arr[i+1]){
        	let temp = arr[i];
            arr[i] = arr[i+1];
            arr[i+1] = temp;
            }
            sortArray(arr, length-1)
            return arr;
          }
          
          
     sortArray([9, 2, 7, 12])     
          1st instance: 9 vs 2.  2 < 9.  9 = temp,  2 = arr[i +1], arr[i] = 2,  arr[i+1] = temp = 9,
          return - [2, 9, 7, 12]
