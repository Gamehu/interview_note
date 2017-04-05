* wait 线程挂起释放锁
* sleep 线程休眠让出cpu，不释放锁
* join 线程按顺序执行，如有t1、t2线程
  t1启动后，调用join()方法，直到t1的任务结束，才轮到t2启动，然后t2也开始任务。，两个线程就按着严格的顺序来执行了。 
* notify 唤醒线程，jvm决定唤醒哪一个
* notifyAll 唤醒所有线程 
* yield 使当前线程从执行状态（运行状态）变为可执行态（就绪状态）。cpu会从众多的可执行态里选择，也就是说，当前也就是刚刚的那个线程还是有可能会被再次执行到的，并不是说一定会执行其他线程而该线程在下一次中不会执行到了。


> 线程的生命周期里有三个状态Runable、Blocked、Running
  yield：Running  ->  Runable
  sleep: Running -> Blocked -> Runable
  yield和sleep都是在线程处于Running的时候开始的，yield只是让出分配给自己的CPU时间片，并且会立刻进入Runable状态参与CPU时间的竞争，若程序中没有其他线程，那么该线程马上就会开始往下执行；sleep会进入Blocked状态，等待时间结束事件的发生，然后进入Runable状态参与CPU时间的竞争
  调用yield的时候锁并没有被释放
  另外，sleep和yield都不具备同步语义，也就是说编译器在执行sleep或yield方法之前和之后，都没有强制要求同步本地缓存与主存的数据
