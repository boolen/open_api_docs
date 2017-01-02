# open_api_docs
Convertlab公司DM Hub产品的开发API文档
- - - 
    
## 目录结构解析
* mkdocs.yml: 总配置，包括主题模式、Github路径、各目录结构层次等。 
* docs目录: 存放所有md文件等地方。
* test目录: api中swaggerui所在目录的所有内容，用于在线测试。

- - -  
## 部署到github pages上的方法
1. 安装mkdocs, apt-get/homebrew。
2. 在与mkdocs.yml同级的路径下执行"rm -r site/"。
3. 执行"mkdocs build", 生成site目录。
3. 执行"cp -r test/ site/", 将test文件夹替换至site目录中的test文件夹。
4. 执行"ghp-import -p site/", 用ghp-import工具将最新代码提交到github上的gh-pages分支，并将site目录打包并上传到github pages服务器。
5. 打开github网页http://site.51convert.cn/open_api_docs/查看部署结果。
