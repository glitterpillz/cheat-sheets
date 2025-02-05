# 🌻 DNSA PROBLEMS - Interview Prep


<br>

## 🐝 1 • Two Sum

### practice basic array manipulations

```javascript
FUNCTION twoSum(nums, target):
    CREATE empty hashmap numMap  // To store numbers and their indices

    FOR each index i and value num in nums:
        SET complement = target - num  // Find required number to reach target

        // If complement exists in hashmap, return indices
        IF complement exists in numMap:
            RETURN [numMap[complement], i]

        // Otherwise, store current number and index in hashmap
        STORE num in numMap with value i

    RETURN []  // This line won't be reached (one solution is guaranteed)
```


<br>

## 🐝 2 • Subarray Sum Equals K

### Find the total number of continuous subarrays whose sum equals K

```javascript
FUNCTION subarraySum(nums, k):
    SET count = 0
    SET prefixSum = 0
    CREATE hashmap prefixMap with {0: 1}  // Handles subarrays starting from index 0

    FOR each num in nums:
        prefixSum += num  // Add current number to prefix sum

        // If (prefixSum - k) exists in hashmap, add its count to result
        IF (prefixSum - k) exists in prefixMap:
            count += prefixMap[prefixSum - k]

        // Store/update prefixSum count in hashmap
        prefixMap[prefixSum] = prefixMap[prefixSum] + 1 (or initialize to 1 if undefined)

    RETURN count
```