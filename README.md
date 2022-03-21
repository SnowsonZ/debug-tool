### fp.tar
- CPU火焰图工具。主要用来采样分析jvm进程CPU调用。使用到以下三方库
```
https://github.com/uber-common/jvm-profiler.git
https://github.com/brendangregg/FlameGraph.git
```
- 环境依赖
1. linux
2. python3

- 使用方法：
1. agent方式将jvm-profiler-1.0.0.jar挂在目标jvm进程
```
-javaagent:jvm-profiler-1.0.0.jar=sampleInterval=5000
```
2. ./fp.sh 采样数据文件路径
```
eg: ./fp.sh /var/log/flink.task-app.out
```
3. out目录生成对应火焰图。