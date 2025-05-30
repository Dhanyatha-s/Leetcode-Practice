# Leetcode Practice

<h4>Easy Types</h4>

<table>
  <tr>
    <td width="50%">
      <h3>Duplicate Value</h3>
      <p><i>Description: <br>
        input = nums = [1,2,3,1]<br>
        output =  True
      </p>
      <p><a href="[https://leetcode.com/problems/contains-duplicate/](https://leetcode.com/problems/contains-duplicate/)">LeetCode Link</a></p>
      <p><strong>Difficulty:</strong> Easy</p>
      <p><strong>Tags:</strong> Array, Hash Table</p>
      <p><strong>Approach:</strong> Use a hash set to keep track of seen numbers.</p>
      <p><strong>Time Complexity:</strong> O(n)</p>
      <p><strong>Space Complexity:</strong> O(n)</p>
    </td>
    <td>
      <pre>
      ```python
      def duplicate_value(nums):
        seen = {}
        for n in nums:
          if n in seen:
            return True
          seen[n] = True
        return False
      ```
      </pre>
    </td>
  </tr>
</table>
<table>
  <tr>
    <td width="50%">
      <h3>Two Sum</h3>
      <p><i>Description: <br>
        Given an array of integers `nums` and an integer `target`, return indices of the two numbers such that they add up to `target`.
        You may assume that each input would have exactly one solution, and you may not use the same element twice.
        You can return the answer in any order.
      </p>
      <p><i>Example: <br>
        input: nums = [2,7,11,15], target = 9<br>
        output: [0,1] (because 2 + 7 = 9)
      </p>
      <p><a href="https://leetcode.com/problems/two-sum/">LeetCode Link</a></p>
      <p><strong>Difficulty:</strong> Easy</p>
      <p><strong>Tags:</strong> Array, Hash Table</p>
      <p><strong>Approach:</strong> Use a hash map to store each number and its index. For each number, check if `target - number` exists in the hash map.</p>
      <p><strong>Time Complexity:</strong> O(n)</p>
      <p><strong>Space Complexity:</strong> O(n)</p>
    </td>
    <td>
      <pre>
      python
      def twoSum(nums: list[int], target: int) -> list[int]:
        num_map = {}
        for index, num in enumerate(nums):
          complement = target - num
          if complement in num_map:
            return [num_map[complement], index]
          num_map[num] = index
        return [] 
      </pre>
    </td>
  </tr>
</table>
<table>
  <tr>
    <td width=50%>
      <h3>Missing Value</h3>
      <p><i>Description: <br>
        Given an array `nums` containing `n` distinct numbers in the range `[0, n]`, return the only number in the range that is missing from the array.
      </p>
        <p><i>Example <br>
        input: nums = [3,0,1] <br>
        output: 2
        </p>
          <p><i>Example 2: <br>
        input: nums = [0,1]<br>
        output: 2 (n=2 since there are 2 numbers, so all numbers are in the range [0,2]. 2 is the missing number in the range since it does not appear in nums.)
      </p>
      <p><i>Example 3: <br>
        input: nums = [9,6,4,2,3,5,7,0,1]<br>
        output: 8 (n=9 since there are 9 numbers, so all numbers are in the range [0,9]. 8 is the missing number in the range since it does not appear in nums.)
      </p>
        <p><a href="https://leetcode.com/problems/missing-number/">LeetCode Link</a></p>
      <p><strong>Difficulty:</strong> Easy</p>
      <p><strong>Tags:</strong> Array, Hash Table, Math, Bit Manipulation, Sorting</p>
      
   <p><strong>Time Complexity (Summation):</strong> O(n)</p>
    
  </td>
        <td>
          <pre>
            python
            def missinf_value(nums: list[int]) -> int:
               nums.sort()
               for i, v in enumerate(nums):
                  if i != v:
                     return v-1
                  if v == len(nums):
                     return v+1
               return None
          </pre>
        </td>
  </tr>
  
</table>
