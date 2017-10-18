1、node中可以直接require json文件
比如说我们有个json文件，a.json
那么在index.js中可以直接
var a=require（‘a.json’）；
而在a.json中不必用module.exports来导出。


2、写文件
1）fs.write(fd, string[, position[, encoding]], callback)，用这种方式写文件要先用fs.open打开文件，打开文件后会得到一个fd，也就是fs.write的第一个参数，是整数
2、fs.writeFile(file, data[, options], callback)，直接写，不需要用fs.open先打开
写文件有几种方式，比如可以追加，或者全部重写等（http://nodejs.cn/api/fs.html#fs_fs_open_path_flags_mode_callback）
