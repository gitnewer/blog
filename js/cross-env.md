跨平台设置环境变量

# cross-env 

cross-env NODE_ENV=production webpack --config build/webpack.config.js

使用$做字面量的时候，需要用转义符，如果value是json结构，也要用转义符

# cross-env-shell

这个可以把命令作为一个参数启动，在需要执行多个命令组成的序列的时候，适合用这个
