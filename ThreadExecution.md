# Prevent Thread Execution 

# How many ways you can prevent thread execution ?
  1. sleep()
  2. yield()
  3. join() 
# What is the purpose Thread.yield() 
 analogy : Long call in the Phone booth , and someone waiting to get his/her turn to convey an urgent message 
  - yield() method causes to pause current executing thread , to give the chance for the waiting thread of same priority 
  - If there is no waiting thread or all waiting thread have low priority , then same thread can continue excution. 
  - If multiple threads are waiting with same priority then which thread will get the chance we can not expect , it depends on Thread scheduler
  - The Thread which is yielded , when it will get the chance once again , it depends on TS, and we can predict 
  - It is at Thread class ```Pubic static native void yield () ```
  - It is a native method, So some platform doesn't provide proper support for yield method 
