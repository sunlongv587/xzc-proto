# xzc-proto
xzc-proto

### protobufjs

https://github.com/protobufjs/protobuf.js/tree/master/cli#pbts-for-typescript


```
# 下面这个命令不好使了，
npm install protobufjs-cli
# 项目根目录，下安装
npm install protobufjs
cd ./node_modules/protobufjs/cli/bin
# 转成json
node pbjs -t json ~/Codes/githubProjects/xzc-proto/xzc/common/error_body.proto ~/Codes/githubProjects/xzc-proto/xzc/common/xzc_error_code.proto > bundle.json
# 打包成静态js
node pbjs -t static-module -w commonjs -o compiled.js ~/Codes/githubProjects/xzc-proto/xzc/common/error_body.proto ~/Codes/githubProjects/xzc-proto/xzc/common/xzc_error_code.proto
# 转成 ts
node pbts -o compiled.d.ts compiled.js
```

### java 

```
# 直接编译jar包到本地 maven repository
mvn install
```