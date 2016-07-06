[TOC]

# HEXO的安装

## 

* 环境：centos6.5 +lnmp node.js  git hexo

## 

##  node.js 安装

### 二进制安装

```
wget https://nodejs.org/dist/v6.2.2/node-v6.2.2-linux-x64.tar.xz
tar xf node-v6.2.2-linux-x64.tar.xz
cd /usr/local/src/node-v6.2.2-linux-x64/bin
[root@duzctest bin]# ls
node  npm


```

* 加入环境变量

  ```
  vim /etc/environment
  PATH=$PATH:/usr/local/src/node-v6.2.2-linux-x64/bin
  ##运行脚本
  source /etc/environment
  [root@duzctest etc]# node -v
  v6.2.2
  ```

## gitub

## hexo

### 安装

```
npm install hexo-cli -g
```

* 安装后的tree

  ```
  /usr/local/src/node-v6.2.2-linux-x64/lib
  └─┬ hexo-cli@1.0.2 
    ├── abbrev@1.0.9 
    ├── bluebird@3.4.1 
    ├─┬ chalk@1.1.3 
    │ ├── ansi-styles@2.2.1 
    │ ├── escape-string-regexp@1.0.5 
    │ ├─┬ has-ansi@2.0.0 
    │ │ └── ansi-regex@2.0.0 
    │ ├── strip-ansi@3.0.1 
    │ └── supports-color@2.0.0 
    ├─┬ hexo-fs@0.1.6 
    │ ├─┬ chokidar@1.6.0 
    │ │ ├─┬ anymatch@1.3.0 
    │ │ │ ├── arrify@1.0.1 
    │ │ │ └─┬ micromatch@2.3.10 
    │ │ │   ├─┬ arr-diff@2.0.0 
    │ │ │   │ └── arr-flatten@1.0.1 
    │ │ │   ├── array-unique@0.2.1 
    │ │ │   ├─┬ braces@1.8.5 
    │ │ │   │ ├─┬ expand-range@1.8.2 
    │ │ │   │ │ └─┬ fill-range@2.2.3 
    │ │ │   │ │   ├── is-number@2.1.0 
    │ │ │   │ │   ├── isobject@2.1.0 
    │ │ │   │ │   ├── randomatic@1.1.5 
    │ │ │   │ │   └── repeat-string@1.5.4 
    │ │ │   │ ├── preserve@0.2.0 
    │ │ │   │ └── repeat-element@1.1.2 
    │ │ │   ├─┬ expand-brackets@0.1.5 
    │ │ │   │ └── is-posix-bracket@0.1.1 
    │ │ │   ├── extglob@0.3.2 
    │ │ │   ├── filename-regex@2.0.0 
    │ │ │   ├─┬ kind-of@3.0.3 
    │ │ │   │ └── is-buffer@1.1.3 
    │ │ │   ├── normalize-path@2.0.1 
    │ │ │   ├─┬ object.omit@2.0.0 
    │ │ │   │ ├─┬ for-own@0.1.4 
    │ │ │   │ │ └── for-in@0.1.5 
    │ │ │   │ └── is-extendable@0.1.1 
    │ │ │   ├─┬ parse-glob@3.0.4 
    │ │ │   │ ├── glob-base@0.3.0 
    │ │ │   │ └── is-dotfile@1.0.2 
    │ │ │   └─┬ regex-cache@0.4.3 
    │ │ │     ├── is-equal-shallow@0.1.3 
    │ │ │     └── is-primitive@2.0.0 
    │ │ ├── async-each@1.0.0 
    │ │ ├── glob-parent@2.0.0 
    │ │ ├── inherits@2.0.1 
    │ │ ├─┬ is-binary-path@1.0.1 
    │ │ │ └── binary-extensions@1.5.0 
    │ │ ├─┬ is-glob@2.0.1 
    │ │ │ └── is-extglob@1.0.0 
    │ │ ├── path-is-absolute@1.0.0 
    │ │ └─┬ readdirp@2.1.0 
    │ │   ├─┬ minimatch@3.0.2 
    │ │   │ └─┬ brace-expansion@1.1.5 
    │ │   │   ├── balanced-match@0.4.1 
    │ │   │   └── concat-map@0.0.1 
    │ │   ├─┬ readable-stream@2.1.4 
    │ │   │ ├── buffer-shims@1.0.0 
    │ │   │ ├── core-util-is@1.0.2 
    │ │   │ ├── isarray@1.0.0 
    │ │   │ ├── process-nextick-args@1.0.7 
    │ │   │ ├── string_decoder@0.10.31 
    │ │   │ └── util-deprecate@1.0.2 
    │ │   └── set-immediate-shim@1.0.1 
    │ └── graceful-fs@4.1.4 
    ├─┬ hexo-log@0.1.2 
    │ └─┬ bunyan@1.8.1 
    │   ├─┬ dtrace-provider@0.6.0 
    │   │ └── nan@2.3.5 
    │   ├── moment@2.14.1 
    │   ├─┬ mv@2.1.1 
    │   │ ├─┬ mkdirp@0.5.1 
    │   │ │ └── minimist@0.0.8 
    │   │ ├── ncp@2.0.0 
    │   │ └─┬ rimraf@2.4.5 
    │   │   └─┬ glob@6.0.4 
    │   │     ├─┬ inflight@1.0.5 
    │   │     │ └── wrappy@1.0.2 
    │   │     └── once@1.3.3 
    │   └── safe-json-stringify@1.0.3 
    ├─┬ hexo-util@0.6.0 
    │ ├─┬ camel-case@3.0.0 
    │ │ ├─┬ no-case@2.3.0 
    │ │ │ └── lower-case@1.1.3 
    │ │ └── upper-case@1.1.3 
    │ ├─┬ cross-spawn@4.0.0 
    │ │ ├─┬ lru-cache@4.0.1 
    │ │ │ ├── pseudomap@1.0.2 
    │ │ │ └── yallist@2.0.0 
    │ │ └─┬ which@1.2.10 
    │ │   └── isexe@1.1.2 
    │ ├── highlight.js@9.5.0 
    │ ├── html-entities@1.2.0 
    │ └── striptags@2.1.1 
    ├── minimist@1.2.0 
    ├── object-assign@4.1.0 
    └─┬ tildify@1.2.0 
      └── os-homedir@1.0.1 

  ```

  ```
  npm install hexo-cli -g
  hexo init blog
  cd blog
  npm install
  hexo server
  ```

  ​

### 源码包安装



```
#下载
wget https://nodejs.org/dist/v4.4.7/node-v4.4.7.tar.gz
tar xf node-v4.4.7.tar.gz
cd node-v4.4.7


```

