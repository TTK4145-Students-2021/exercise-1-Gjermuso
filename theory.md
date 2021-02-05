Exercise 1 - Theory questions
-----------------------------
 
 ### What is the difference between concurrency and parallelism?
 > Concurrency is where you perform multiple tasks at the same time, but on a single thread. The tasks then shares the processing power, but does not compute at the same time, just alternating the computations. Parallelism is where you perform multiple tasks on multiple threads, allowing you to compute multiple tasks at the same time no waiting for the other task to free up the processor).
 
 ### Why have machines become increasingly multicore in the past decade?
 > Having extra cores allows your processor to work more efficiently in regards to both speed and energy consumption. Breaking down complex tasks to smaller comutations that can run individually on multiple cores turns out to be faster since the clockspeed of a single processor cannot exceed certain limits before being bottlenecked by overheating and such. Having then i.e. two cores running at 3GHz will have more power than one running at 5GHz. This however, depends on the machines ability to divide complex tasks into smaller pieces, which is a lot more complex for the programmers making the algorithms. 
 
 ### Why do we divide software (programs) into concurrently executing parts (like threads or processes)?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Concurrency may help reduce the timings where each computation is done. Concurrency may also be used to reduce read-write and write-write conflicts i memory as the data will be used by several programs at the same time before changing it for the next program. 
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Concurrent programs are famous for being a pain to work with.
 
 ### What is the conceptual difference between threads and processes?
 > A process is a program under excecution. The process is complex and not lightweight, whereas a thread is lightweight and a part of a process and a process can have multiple threads. 
 
 ### Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they?
 > Fibers are particularly lightweight threads that use cooperative multitasking, not preemptive multitasking. Preemtive multitasking is where the task is claiming the processors and pausing the current task. Cooperative multitasking is a bit more gentle approach where the task is asking to use the processor when the current task is done or on a pause. 
 
 ### What is the Go-language's "goroutine"? A C/POSIX "pthread"?
 > A "goroutine" is a lightweight thread in go. It is capaple of running cocurrently with other goroutines. 
 A pthread is basically the same thing, but works independently of any programming language.
 
 ### In Go, what does `func GOMAXPROCS(n int) int` change? 
 > The function changes the maximum number of processors that can work simultaneously.



 
 
 
 
