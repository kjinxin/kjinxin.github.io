---
layout: post
comments: true
categories: C++
---
## Split string with space
    istringstream ss(st);
    vector<string> tokens{ istream_iterator<string>{ss}, istream_iterator<string>{}};
