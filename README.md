# logger
日志打印工具

### 日志等级
```
DEBUG   debug信息  0
FUNC    方法信息   1 
INFO    普通信息   2
CONFIG  配置信息   3
ERROR   错误信息   4
FATAL   致命信息   5
```

### 使用 

- 直接使用

```
func main() {
	logger.Error("this is error")
	logger.Config("this is config")
	logger.Debug("this is debug")
	logger.Info("this is info")
	logger.Func("this is func")
	logger.Fatal("this is fatal")
}
```
!["效果1"](https://raw.githubusercontent.com/lhlyu/logger/master/img/console1.jpg)

- 设置低等级日志过滤/日志输出到文本

```
func main() {
	// 设置日志过滤等级 = 3 ，小于 3 的日志不打印
	// 第二个参数可以设置输出文本文件夹的地址，空字符串表示打印到控制台
	logger.SetLogger(logger.NewLogger(3,""))
	logger.Error("this is error")
	logger.Config("this is config")
	logger.Debug("this is debug")
	logger.Info("this is info")
	logger.Func("this is func")
	logger.Fatal("this is fatal")
}
```
!["效果1"](https://raw.githubusercontent.com/lhlyu/logger/master/img/console2.jpg)
