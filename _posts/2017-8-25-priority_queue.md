---
layout: post
comments: true
categories: C++
---
## priority_queue
Define a class Compare and overload Operator() like this:

    class Foo
    {

    };

    class Compare
    {
    public:
        bool operator() (Foo, Foo)
        {
            return true;
        }
    };

    int main()
    {
        std::priority_queue<Foo, std::vector<Foo>, Compare> pq;
        return 0;
    }

If we do not want to define compare class, we could use std::function
    class Foo
    {

    };

    bool Compare(Foo, Foo)
    {
        return true;
    }

    int main()
    {
        std::priority_queue<Foo, std::vector<Foo>, std::function<bool(Foo, Foo)>> pq(Compare);
        return 0;
    }
