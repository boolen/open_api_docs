# open_api_docs
Convertlab公司DM Hub产品的开发API文档
- - - 
    
## 目录结构解析
* mkdocs.yml: 总配置，包括主题模式、Github路径、各目录结构层次等。 
* docs目录: 存放所有md文件等地方。
* test目录: api中swaggerui所在目录的所有内容，用于在线测试。

- - -  
## 部署方法
1. 安装mkdocs, apt-get/homebrew
2. 在与mkdocs.yml同级的路径下之行"mkdocs build"，生成site目录
3. 将test目录覆盖到site中的test目录中
4. 最后将site目录部署在web服务器上
