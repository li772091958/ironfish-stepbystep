# ironfish-stepbystep
## 前置环境
:exclamation::exclamation:gcc、g++、make，版本过低就更新下，自行百度吧
```
apt update
apt install gcc g++ make
```

## 安装node
```
mkdir /module
cd /module
wget https://npmmirror.com/mirrors/node/v16.13.1/node-v16.13.1-linux-x64.tar.xz
tar xf node-v16.13.1-linux-x64.tar.xz -C ./node

```

## 环境变量
 运行`vim ~/.bashrc`编辑文件，在最后添加下面一行  
 
:rage::rage:注意，这里不仅添加了node和npm的全局命令:rage::rage:  
:rage::rage:还添加了ironfish-cli，需要下面所有步骤完成ironfish的命令才可以正常使用:rage::rage:
 
 ```
 export PATH=$PATH:/module/node/bin:/opt/ironfish/ironfish-cli/bin
 ```

 保存后运行`source ~/.bashrc`使生效

 测试node环境是否OK

 ```
 node -v
 npm -v

 ```
 
 ## 全局安装yarn
 ```
 npm i yarn -g
 ```
 
 ## 安装Rust
 ```
 curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
 ```

## 下载ironfish源代码
```
 mkdir /opt && cd /opt
 git clone https://github.com/iron-fish/ironfish.git
```

## 编译ironfish-rust-nodejs
```
cd /opt/ironfish/ironfish-rust-nodejs
yarn
yarn build
```

## 安装编译ironfish依赖包
```
cd /opt/ironfish
yarn
```

## 后续操作
:+1::+1::bikini:以上所有完成后，ironfish就算安装完成了，接下来的操作就跟着官方文档弄。:bikini::+1::+1:  
  
[启动新节点](https://ironfish.network/docs/onboarding/start-an-iron-fish-node)
