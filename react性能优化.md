http://www.cnblogs.com/YikaJ/p/4912187.html
http://www.cocoachina.com/webapp/20150902/13316.html
1、shouldComponentUpdate判断组件是否需要更新
2、shouldComponentUpdate存在的问题，如果被判断的是引用类型，因为都是同一个内存地址，所以可能出现即使状态改变了，也不刷新（因为改变前后都是指向同一地址）。
3、shouldComponentUpdate的mixin----pureRenderMixin。这个mixin会自动调用shouldComponentUpdate方法来比较现在的state和props是否有改变。使用方法：http://blog.csdn.net/qq_18661257/article/details/68950801
4、shouldComponentUpdate的问题可以用深拷贝来解决（loadash 中提供了深拷贝函数）loadash：https://lodash.com/docs#cloneDeep
5、深拷贝也有自己的性能问题，用immutable.js来解决。https://github.com/camsong/blog/issues/3
官网：http://facebook.github.io/immutable-js/

5.1）immutablejs一旦生成一个数据，那这个数据就不能再被改变。
5.2）一旦数据有改变，则会新生成一个数据，原来的数据不会改变。
5.3）新生成的数据并不是完全保存下来的，而是保存的与原来的数据的“差异”。这样可以节省空间，并提升性能。
6、将immutable加入工程中：http://react-china.org/t/react-redux-immutablejs/9948
7、immutablejs和pureRenderMixin结合使用：http://www.cnblogs.com/YikaJ/p/4912187.html这篇文章的底部。
