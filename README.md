# xzc-proto
xzc-proto

### google-protobuf

```

protoc --proto_path=./ --js_out=import_style=commonjs,binary:build ./xzc/common/* ./xzc/account/* ./xzc/room/* ./xzc/game/* 
```

### protobufjs（无法支持Any对象的传输，弃用）
### 开源地址
https://github.com/protobufjs/protobuf.js/tree/master/cli#pbts-for-typescript
### 教程
https://mp.weixin.qq.com/s/8KA6wYdFLWnaLfvgf82k7g

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
node pbjs -t static-module -w commonjs -o xzc-proto.js -p ../../../../xzc/common/* ../../../../xzc/room/* ../../../../xzc/game/* ../../../../xzc/account/*
# 转成 ts
node pbts -o compiled.d.ts compiled.js
node pbts -o xzc-proto.d.ts xzc-proto.js
```

### java 

```
# 直接编译jar包到本地 maven repository
mvn install
```