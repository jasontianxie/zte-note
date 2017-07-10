http://www.cnblogs.com/YikaJ/p/4912187.html
1、shouldComponentUpdate判断组件是否需要更新
2、shouldComponentUpdate存在的问题，如果被判断的是引用类型，因为都是同一个内存地址，所以可能出现即使状态改变了，也不刷新（因为改变前后都是指向同一地址）。
3、shouldComponentUpdate的mixin----pureRenderMixin
4、shouldComponentUpdate的问题可以用深拷贝来解决（loadash 中提供了深拷贝函数）loadash：https://lodash.com/docs#cloneDeep
5、深拷贝也有自己的性能问题，用immutable.js来解决
