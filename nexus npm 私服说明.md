https://www.npmjs.com/

npm 缓存位置 C:\Users\cy\AppData\Roaming\npm-cache ; 清空缓存命令 `npm cache clean`

nexus安装并创建npm仓库后，仓库位置：C:\t\nexus\sonatype-work\nexus\storage\cnpm

下载并安装hbase-client包
npm i --registry=http://localhost:8081/nexus/content/repositories/cnpm/ hbase-client
 -g 全局安装。

设置默认的仓库地址
`npm config set registry http://localhost:8081/nexus/content/repositories/cnpm/`

nexus安装为windows服务
cd C:\t\nexus\nexus-2.13.0-01\bin

`nexus install`

`nexus start`
