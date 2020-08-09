## 后台
`
MISCONF Redis is configured to save RDB snapshots, but is currently not able to persist on disk. Commands that may modify the data set are disabled. Please check Redis logs for details about the error.
`

redis中执行:`config set stop-writes-on-bgsave-error no`
参考链接: [https://www.jianshu.com/p/3aaf21dd34d6](https://www.jianshu.com/p/3aaf21dd34d6)

## 判题机
关于判题结果中的Presentation Error这个错误的话，我们使用 Linux 的 `diff` 程序比较程序输出和参考答案，如果开启 `-Z` 选项找不到差异，那么是 Accepted；否则，如果开启 `-a -w -B` 选项找不到差异，那么是 Presentation Error；否则，是 Wrong Answer。这些选项的具体含义如下：
```
    -Z, --ignore-trailing-space
           ignore white space at line end

    -a, --text
           treat all files as text

    -w, --ignore-all-space
           ignore all white space

    -B, --ignore-blank-lines
           ignore changes whose lines are all blank
```
常见的导致 Presentation Error（甚至 Wrong Answer）的情况有：
1. 输出多个数字时，忘记输出空格或换行。
2. 使用 `fwrite` 时，输出长度计算错误，多输出了一个 `\0`。
3. 使用 `%I64d` 输出 `long long int` 类型的整数。这个写法不规范，在有的平台上相当于 `%64d`，导致输出了 `32` 位整数，而且在整数前面补了若干个空格，还会使其后面的参数错位。应该使用 `%lld`。


## 编辑器
Windows 下面的的默认的换行是`\r\n`，假如在测试样例里面依旧使用这样的格式的话，上传上去的测试数据会被后台替换成`\n`
![vscode的显示效果](https://github.com/4ddl/docs/blob/master/TIM%E6%88%AA%E5%9B%BE20200809113410.png?raw=true)
Linux 下面的话虽然默认是`\n`，写一个文本的话，会被编辑器默认在最后再加上一个`\n`
![vim的显示效果](https://github.com/4ddl/docs/blob/master/TIM%E6%88%AA%E5%9B%BE20200809113753.png?raw=true)
可以参考下知乎里面的回答[https://www.zhihu.com/question/22808787](https://www.zhihu.com/question/22808787)
