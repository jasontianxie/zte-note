react-router-redux到底有什么用？

官方建议使用 redux-simple-router, https://github.com/rackt/redux-simple-router 其实目的也很简单，就是希望一个 APP 只有一个 state 而路由自然也是 state 的一部分， 使用这个类库可以同步 react-router 中的 router 信息到 redux 的 state 中统一管理。

路径http://localhost:3000/#/chatWindow?_k=3dlsrf。在实验中使用console.log（state.routing）得到的结果如下：
locationBeforeTransitions:
Object
$searchBase:
Object
action:"PUSH"
hash:""
key:"3dlsrf"
pathname:"/chatWindow"
query:Object
search:""
state:null
__proto__:Object
__proto__:Object


react-router-redux地址：https://github.com/reactjs/react-router-redux
里面有一些例子，但是都没有讲到怎么用state.routing
目前还没有发现什么场景是要必须用react-router-redux的。
