一、
fetch：https://segmentfault.com/a/1190000003810652
fetch获取服务端的返回值用下面的方法：
fetch('http://127.0.0.1:9002/1/data.json').then(function(response) {
            return response.json();
        }).then(function(data) {
            console.log(data);
        }).catch(function(e) {
            console.log("Oops, error");
        });
要先用json方法转换一次，再获取data。
