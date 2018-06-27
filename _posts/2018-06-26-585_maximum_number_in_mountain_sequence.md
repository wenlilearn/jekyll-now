---
layout: post
permalink: /585_maximum_number_in_mountain_sequence.html
---

# 585. Maximum Number in Mountain Sequence

## Description
Given a mountain sequence of n integers which increase firstly and then decrease, find the mountain top.

## Example
`Given nums = [1, 2, 4, 8, 6, 3] return 8`
`Given nums = [10, 9, 8, 7], return 10`

## Solution
- 这题目一开始直接看暴力解法就是把整个数组遍历一遍, 当碰到后面的元素小于前面的元素的时候, 就return这个元素, 那么这个解法时间复杂度是O(n)的
- 换一种思路, 每次找到一个元素, 我们就看它左右两边的元素
  - 如果大于, 那么我们就继续向右(换句话来说, 舍弃左边的一半)
  - 如果小于, 那么我们就向左(换句话来说, 舍弃右边的一半)
- 这样最后会剩下两个元素, 我们只要比较一下他们俩的大小然后找到比较大的那一个就行了
