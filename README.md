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
    
    
     
    
    

