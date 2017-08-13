1、config-lite:
config-lite 是一个轻量的读取配置文件的模块。config-lite 会根据环境变量（NODE_ENV）的不同从当前执行进程目录下的 config 目录加载不同的配置文件。如果不设置 NODE_ENV，则读取默认的 default 配置文件，如果设置了 NODE_ENV，则会合并指定的配置文件和 default 配置文件作为配置，config-lite 支持 .js、.json、.node、.yml、.yaml 后缀的文件。
引入：var config = require('config-lite');
下面引用config的默认default配置时，提示找不到配置信息，
最新的config-lite用法是：
var config = require('config-lite')(__dirname);

2、pinyin
转换中文字符为拼音。可以用于汉字注音、排序、检索。
