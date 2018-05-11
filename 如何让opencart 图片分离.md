# 如何让opencart 图片分离? 

How to separate the opencart image?

# 实现思路:
在前后台config.php文件中，添加图片域名;
将判断本地图片是否存在去掉;
将所有显示'图片'的域名改为专门的图片域名地址;

后台图片 common/filemanager, 保留本地图片路径;

单独图片域名服务器，需要和网站 保持文件传输
unison+inotify实现数据实时双向同步


# 实现方法:
前后台 涉及的文件

config.php    
<pre><code>
define('HTTP_IMAGE_SERVER', 'http://image.***.com/');
</code></pre>
  
catalog/model/tool/image.php
<pre><code>
if ($this->request->server['HTTPS']) {
		return HTTPS_IMAGE_SERVER . 'image/' . $new_image;
 } else {
		return HTTP_IMAGE_SERVER . 'image/' . $new_image;
 }
  </code></pre>
	
其他视具体业务而定:
主要注释这个:
<pre><code>
if (is_file(DIR_IMAGE . $result['image'])) 
</code></pre>
