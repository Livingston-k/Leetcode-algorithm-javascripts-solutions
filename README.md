# LEETCODE JAVASCRIPTS SOLUTIONS 

#### 1. Two Sum 

Given an array of integers `nums` and an integer `target`, return  *indices of the two numbers such that they add up to `target`* .

You may assume that each input would have  ***exactly* one solution** , and you may not use the *same* element twice.

You can return the answer in any order.

**Example 1:**

<pre><strong>Input:</strong> nums = [2,7,11,15], target = 9
<strong>Output:</strong> [0,1]
<strong>Explanation:</strong> Because nums[0] + nums[1] == 9, we return [0, 1].
</pre>

**Example 2:**

<pre><strong>Input:</strong> nums = [3,2,4], target = 6
<strong>Output:</strong> [1,2]
</pre>

**Example 3:**

`<pre><strong>`Input:`</strong>` nums = [3,3], target = 6
`<strong>`Output:`</strong>` [0,1]`</pre>`


 SOLUTION FOR TWO SUM PROBLEM

/**

* @param{number[]}nums
* @param{number}target
* @return{number[]}

 */

vartwoSum=function (nums, target) {

    previous_values = {}

    for (leti=0; i<=nums.length; i++) {

    letcurrentNum=nums[i];

    letneeded=target-currentNum

    index2 = previous_values[needed]

    if (index2 !=null) {

    return [index2, i]

    } else {

    previous_values[currentNum] =i

    }

    }

};
