# Java Multi Threading notes

Process Based and Thread Based multitasking 


 1. What is a Thread ?
   Ans : Single flow of execution is a thread .
 2. Where there are independent jobs to do , multithreading can be used   
 3. Define a thread 
    1. Extending Thread class 
    2. Implementing Runnable interface
    
 4. Thread Scheduler    
     - When Multiple threads have to be executed , then the order of thread execution decided by the Thread scheduler
     - Order is not guarantee  (It varies JVM to JVM , Roundrobin, FCFS)
     - There is no guarantee for exact output , but we can provide sevaral possible output 
 5. Start method belongs to Thread Class (What is difference between t.start() and t.run())
    - This creates the thread and assign the job (that is defined in the run method )
    - t.run() makes a ordinary function call to run(), execution is predictable and sequencial 
    - t.start() does following
     - register the thread to thread scheduler 
     - Perform all other mandatory activities 
     - invoke the run method 
  6. Overload of run method possible ? 
    - Overloading concept possible 
    - Thread class start method only calls the no argument run method only 
  7. If the MyThread class doesn't override the run method then what will happen 
     - Thread class run method will be called and there will be no output. 
     -  If you don't overide the run method then the feature is misutilised 
  8. Overide the start method 
     - New Thread won't be created 
     - It will be an ordinary method call 
     - it is not recomended to override start method 
     -  if the super.start() is called then it will create another thread .  
  9. Thread Life cycle 
      new >> Ready >> Running >> Dead
      simple basic life cycle of thread
  10. If you restart a already started thread then you will get IllegalThreadStateException 
  
  11. Defining a Thread by Implementing Runnable Interface 
     Runnable
        ^
        |
     Thread
        ^
        |
     MyThread   
     
     Runnable
        ^
        |
     MyRunnable (Only Implement Run method)
  12. Implements Runnable vs extend Thread class         
      - In case of extending Thread class we will loose the multiple inheritance . Only Single Inheritance is possible in java   
  13. 8 constructors are there in Thread Class 
  14. Thread.currentThread().getName()
      Thread.currentThread().setName()
  15. Thread Priorities 
        1. Every Thread has a Thread Priorities 
        2. Default Priority set by JVM 
        3. Values ranges from ```1 to 10 ```
        4. MIN priorities 1  // Thread.MIN_PRIORITY
        5. MAX Priorities 10  // Thread.MAX_PRIORITY
        6. NORMAL Priorities 5 // Thread.NORAML_PRIORITY // default for Main , Other inherited from Parent thread
        7. Thread scheduler decides the processor allocation by the the thread priority 
        8. Incase two thread of same priority , Then the execution order is not predictable , it depends on TS
        9. Thread class has final method to set and get Priority (final methods )
        10. If the the priority is not in the range then you wil get IllegalArgumentException 
        
         
      
      
  
  
      
      
  
     
  
  
    
    
     
    
    

