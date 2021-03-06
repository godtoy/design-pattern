#命令设计模式


###1. 模式动机 ###
```
	在软件设计中，我们经常需要向某些对象发送请求，但是并不知道请求的接收者是谁，
也不知道被请求的操作是哪个，我们只需在程序运行时指定具体的请求接收者即可，
此时，可以使用命令模式来进行设计，使得请求发送者与请求接收者消除彼此之间的耦合，让对象之间的调用关系更加灵活。
命令模式可以对发送者和接收者完全解耦，发送者与接收者之间没有直接引用关系，
发送请求的对象只需要知道如何发送请求，而不必知道如何完成请求。这就是命令模式的模式动机。


	Do：
	>将一个请求封装为一个对象，从而使我们可用不同的请求对客户进行参数化；对请求排队或者记录请求日志，以及支持可撤销的操作
		
```

###2.模式优点
-	降低对象之间的耦合度。
-	新的命令可以很容易地加入到系统中。
-	可以比较容易地设计一个组合命令。
-	可以方便管理命令执行的行为和记录一些日志等操作（可管理，可操作性）
-	调用同一方法实现不同的功能

###3.缺点
-	>本科小生：使用命令模式可能会导致某些系统有过多的具体命令类。因为针对每一个命令都需要设计一个具体命令类，因此某些系统可能需要大量具体命令类，这将影响命令模式的使用。



###4.代码
>这里我是看到了【本科小生CSDN】的博客来进行编码的，感觉当中有一些有点和缺点没有体现出来，所以我做了一些自己的思想改动

```
	项目结构说明：
		-	
			1. org.oeynet.*
			2. client 客户端代码
			3. cmd 封装了命令模式的库
			4. start 启动

```



###5.联想和实际开发应用