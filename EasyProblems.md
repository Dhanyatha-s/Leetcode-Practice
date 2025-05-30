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
