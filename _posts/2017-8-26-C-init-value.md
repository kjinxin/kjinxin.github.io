---
layout: post
comments: true
categories: diary
title: C++-init value
---
In C++ class, we should init value in constructer.

For example:

    class TrieNode {

    public: 
        bool isLeaf;
        vector<TrieNode*> child;
        TrieNode(int size) : child(size, NULL) , isLeaf(false) {
        }
    };
