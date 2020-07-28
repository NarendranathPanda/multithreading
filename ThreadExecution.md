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
  - It is at Thread class ```pubic static native void yield () ```
  - It is a native method, So some platform doesn't provide proper support for yield method 
# What is the purpose of t2.join()
  analogy: Two friends going for two different class , One Friend waits for other one to finish , so that they can go home together 
  - If a threads(t1) wants to wait until someother thread(t2) completes it's job then that thread(t1) will call the join method on the other thread(t2.join())
  - When t1 calls t2.join(), immediately it goes into waiting state until t2 finishes 
  - syntax in thread class 
       - ```public final void join() throws InterruptedException``` 
       - ```public final void join(long ms) throws InterruptedException```
       - ```public final void join(long ms, int ns) throws InterruptedException```
  
  - If the waiting thread interrupted by other thread then , it may throw InterruptedException (Checked Exception)
  - When the t2 come out of waiting 
  - t2 completes 
  - time expires
  - waiting thread got interrupted 
  
  -  How child class can wait for main thread to complete  , Get the main thread reference through a static Thread variable 
  
  - Dead lock situation can arise if both thread waits for each other . 
  - Thread.currentThread().join() // The current thread waits for itself // dead lock
  
# Sleep Method
-  If a Thread don't want to perform any job for a specific amount of time , can call sleep() , It pauses the thread from execution 
- ```public static native void sleep(long ms)```
- ```public static void sleep(long ms,int ns)```
- Throws InterruptedException






  
  
  
  
  
  
  
  
