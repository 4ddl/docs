## 后台
`
MISCONF Redis is configured to save RDB snapshots, but is currently not able to persist on disk. Commands that may modify the data set are disabled. Please check Redis logs for details about the error.
`

redis中执行:`config set stop-writes-on-bgsave-error no`
参考链接: [https://www.jianshu.com/p/3aaf21dd34d6](https://www.jianshu.com/p/3aaf21dd34d6)
