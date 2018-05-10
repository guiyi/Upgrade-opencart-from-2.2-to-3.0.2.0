### Upgrade-opencart-from-2.2-to-3.0.2.0
#opencart3.0.0.0版本较之2.x系列版本重要提升点有三：
1. 模板统一采用twig引擎，这将使绝大部分的插件需要重新升级；
2. 后台可以编辑模板代码；
3. 后台可以编辑语言包，这为不同语言文件的处理提供了极大便利，无需再提供专门的语言包；

#升级流程
1.备份网站，数据库；
2.创建一个Test Server
3.导出数据 --插件可选 Excelport2.2
4.导入数据 --插件可选 Excelport3.03
5.迁移扩展和修改--插件可选 NitroPack Cache - Complete Performance Optimization Framework、SEO Backpack - All SEO Tools in One Place
6.域名加载Opencart3.0



#参考链接
http://baijiahao.baidu.com/s?id=1587531043320427606&wfr=spider&for=pc
https://www.opencart.com/blog?blog_id=244 视频
https://www.opencart.com/index.php?route=marketplace/extension/info&extension_id=10197&filter_search=excelport
https://www.opencart.com/index.php?route=marketplace/extension/info&extension_id=12658&filter_search=nitropack