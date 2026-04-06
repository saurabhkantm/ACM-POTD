class MyQueue {
private:
    stack<int> inStack;
    stack<int> outStack;

public:
    MyQueue() {}

    void push(int x) {
        inStack.push(x);
    }

    int pop() {
        peek();                // ensure outStack has elements
        int val = outStack.top();
        outStack.pop();
        return val;
    }

    int peek() {
        if (outStack.empty()) {
            while (!inStack.empty()) {
                outStack.push(inStack.top());
                inStack.pop();
            }
        }
        return outStack.top();
    }

    bool empty() {
        return inStack.empty() && outStack.empty();
    }
};
<img width="1889" height="853" alt="image" src="https://github.com/user-attachments/assets/943d3316-3a79-45b6-9203-60f110075128" />
