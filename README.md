# ironfish-stepbystep
## 安装这些鬼东西
```
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
 ```
 export PATH=$PATH:/module/node/bin:/opt/ironfish/ironfish-cli/bin
 ```

 保存后运行`source ~/.bashrc`使生效

 测试node环境是否OK

 ```
 node -v
 npm -v

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
