* wait 线程挂起释放锁
* sleep 线程休眠让出cpu，不释放锁
* join 线程按顺序执行，如有t1、t2线程
  t1启动后，调用join()方法，直到t1的任务结束，才轮到t2启动，然后t2也开始任务。，两个线程就按着严格的顺序来执行了。 
* notify 唤醒线程，jvm决定唤醒哪一个
* notifyAll 唤醒所有线程 