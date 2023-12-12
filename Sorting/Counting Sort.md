```javascript
function countingSort(arr) {
  // Find the maximum value in the array
  let max = arr[0];
  for (let i = 1; i < arr.length; i++) {
    if (arr[i] > max) {
      max = arr[i];
    }
  }

  // Create an array to store the count of each element
  const count = Array(max + 1).fill(0);

  // Count the occurrences of each element
  for (const num of arr) {
    count[num]++;
  }

  // Reconstruct the sorted array
  let sortedIndex = 0;
  for (let i = 0; i <= max; i++) {
    while (count[i] > 0) {
      arr[sortedIndex] = i;
      sortedIndex++;
      count[i]--;
    }
  }

  return arr;
}

// Example usage
const unsortedArray = [4, 2, 7, 1, 9, 5, 2];
const sortedArray = countingSort(unsortedArray);

console.log("Unsorted Array:", unsortedArray);
console.log("Sorted Array:", sortedArray);
```