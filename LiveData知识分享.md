1. LiveData是什么？
2. LiveData怎么使用？
3. 为什么使用LiveData，LiveData的好处在哪里？
4. LiveData与常规的可观察类有什么不同？
5. LiveData可以存储哪些数据类型？

回答：

1. LiveData是一种可观察的数据存储器类。
2. 在Android中需要先添加LiveData的组件。
	implementation "androidx.lifecycle:lifecycle-viewmodel:$lifecycle_version"
	1. 创建LiveData的实例以存储某种类型的数据。这通常在ViewModel中完成。
	2. 创建可定义的onChanged()方法的Observer对象，该方法可以控制LiveData对象存储的数据更改时会发生什么情况。	

