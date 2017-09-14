---
layout: post
comments: true
categories: 
  LeetCode
  Algorithm
  Cplus
title: Index-Tree
---

    class NumArray {
    public:
        vector<int> Bitree;
        vector<int> nums;
        NumArray(vector<int> nums) : Bitree(nums.size() + 1, 0), nums(nums) {
            for (int i = 0; i < nums.size(); i ++) {
                add(i, nums[i]);
            }
        }

        void update(int i, int val) {
            int diff = val - nums[i];
            add(i, diff);
            nums[i] = val;
        }

        int sumRange(int i, int j) {
            return sumRange(j) - sumRange(i - 1);
        }
    private:
        void add(int i, int val) {
            i ++;
            while(i < Bitree.size()) {
                Bitree[i] += val;
                i += i & (-i);
            }
        }
        int sumRange(int i) {
            int ans = 0;
            i ++;
            while(i > 0) {
                ans += Bitree[i];
                i = i & (i - 1);
            }
            return ans;
        }
    };
