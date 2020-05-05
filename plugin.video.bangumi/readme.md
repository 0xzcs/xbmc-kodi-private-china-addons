# bangumi for kodi 0.1.0(说明还没有写好)
## 🎯简介
- bangumi插件是一个番剧聚合插件，它是vid插件的改进版，为适配番剧网站而生

---
## 内置函数

### get_html()

#### 描述：
get_html() 函数和requests.get函数相同，但是get_html() 函数返回url的网页源代码同时会缓存一份在本地，两分钟内的相同请求直接调用缓存的结果，减少向服务器请求的次数，降低被网站站长察觉的几率

#### 语法：
get_html(url,ua)
####  参数：
参数 | 说明
---- | ----
url | 字符串(str)，必填参数，为要访问的url
ua | 字符串(str)，可选参数，不填默认为pc的ua。

ua可传入的值：

ua值 | 说明
---- | ----
pc | 电脑的ua
mobile | 安卓手机的ua
iphone | 苹果手机的ua
ipad | ipad的ua
mac | 苹果电脑的ua

#### 返回值：
函数返回url的网页源代码
#### 实例：

以下展示了使用 get_html() 方法的实例：
```python
print(get_html('http://so.cn'))
```
以上实例运行后输出结果为：
```html

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta http-equiv="Content-Type" content="text/html; charset=gb2312" />
<title>交易所域名 区块链域名 域名商城</title>
<style type="text/css">
<!--
.STYLE5 {
	font-size: xx-large;
	font-weight: bold;
}
-->
</style>
</head>

<body>
<!--<p align="center"><strong><span class="STYLE2">您所访问的网站域名出售</span></strong></p>
<p align="center">The domain you visiting is asking for sale</p>
<!--<p align="center">域名释义：百花、百画、白华、白桦</p>
<p align="center">电话/TEL：<span lang="EN-US" xml:lang="EN-US">15907387772</span></p>-->
<p align="center">&nbsp;</p>
<p align="center"><span class="STYLE5"><strong>您访问的网站域名可以合作</strong></span> <br />
The domain name you visit can cooperate<br /><br />Domain name holder Dai Yue is a well-known Chinese domain name investor with 16 two-letter .COM domain names. <br />This domain name is on sale. Dai Yue has a team of Chinese domain name brokers to promote and sell these domain names. <br />People with resources from all over the world are welcome to recommend customers to buy domain names. Dai Yue can pay commissions.</p>

                  </div>
              </div>
</div>
            <div id="link-report_group">
                

            </div>
<p align="center">&nbsp;</p>
<p align="center">&nbsp;</p>
<p align="center">联系微信<span lang="EN-US" xml:lang="EN-US"></span>：bieshu</p>
<!--<p align="center">E-MAIL:<a href="mailto:66998111@QQ.COM">66998111@QQ.COM</a></p>
<p align="center">&nbsp;</p>
<p align="center"><a target="_blank" href="http://wpa.qq.com/msgrd?v=3&uin=200575675&site=qq&menu=yes"><img border="0" src="http://wpa.qq.com/pa?p=2:200575675:41" alt="点击这里给我发消息" title="点击这里给我发消息"/></a></p>-->
<p align="center"><img src="weixin.jpg" width="171" height="227" /></p>
<p align="center">扫描二维码添加我微信</p>
<p align="center">E-mail：<a href="mailto:79758@qq.com">79758@qq.com</a></p>
<p align="center">&nbsp;</p>
<p align="center">&nbsp;</p>
<p align="center">&nbsp;</p>
<p align="center">&nbsp;</p>
<p align="center">友情链接：<a href="http://www.yuming.com">域名商城 </a>&nbsp;<a href="http://www.loupan.com">楼盘网 </a></p>
<!--<<div align="center">
  <script language="javascript" type="text/javascript" src="//js.users.51.la/19152566.js"></script>
  <noscript>
  <a href="//www.51.la/?19152566" target="_blank"><img alt="&#x6211;&#x8981;&#x5566;&#x514D;&#x8D39;&#x7EDF;&#x8BA1;" src="//img.users.51.la/19152566.asp" style="border:none" /></a>
  </noscript>
</div>-->
<p align="center">&nbsp;</p>
<div align="center">
  <script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?87fd4b3d3045969f2152b7a5f8121d55";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>
  <script type="text/javascript">var cnzz_protocol = (("https:" == document.location.protocol) ? "https://" : "http://");document.write(unescape("%3Cspan id='cnzz_stat_icon_1277143880'%3E%3C/span%3E%3Cscript src='" + cnzz_protocol + "s23.cnzz.com/z_stat.php%3Fid%3D1277143880%26show%3Dpic' type='text/javascript'%3E%3C/script%3E"));</script>
</div>
</body>
</html>

```
### post_html()

#### 描述：
post_html() 函数和requests.post函数相同，但是post_html() 函数返回url的网页源代码同时会缓存一份在本地，两分钟内的相同请求直接调用缓存的结果，减少向服务器请求的次数，降低被网站站长察觉的几率

#### 语法：
post_html(url,data,ua)
####  参数：
参数 | 说明
---- | ----
url | 字符串(str)，必填参数，为要访问的url
data | 字符串化的字典(str(dict))，必填参数，为要post的值组成的字典
ua | 字符串(str)，可选参数，不填默认为pc的ua。

ua可传入的值：

ua值 | 说明
---- | ----
pc | 电脑的ua
mobile | 安卓手机的ua
iphone | 苹果手机的ua
ipad | ipad的ua
mac | 苹果电脑的ua

#### 返回值：
函数返回url的网页源代码
#### 实例：

以下展示了使用 post_html() 方法的实例：
```python
payload = str({'key1': 'value1', 'key2': 'value2'})

print(post_html('https://httpbin.org/post',payload))
```
以上实例运行后输出结果为：
```json
"form": {
    "key2": "value2",
    "key1": "value1"
  },
```

### unix_to_data()

#### 描述：
unix_to_data()返回人类能正常理解的unix时间

#### 语法：
unix_to_data(uptime,format)
####  参数：
参数 | 说明
---- | ----
uptime | 整数(int)，必填参数，为要转换的unix时间（10位或者13位）
format | 字符串(str)，可选参数，不填默认输出 2020-10-10格式的时间。

format可传入的值：

format值 | 说明
---- | ----
data | 输出 2020-10-10格式的时间
zhdata | 输出 2020年10月10日 格式的时间
datatime | 输出 2020-10-10 10:10:10 格式的时间
zhdatatime | 输出 2020年10月10日 10时10分10秒 格式的时间
time | 输出 10:10:10 格式的时间
zhtime | 输出 10时10分10秒 格式的时间

#### 返回值：
函数返回人类能正常理解的unix时间
#### 实例：

以下展示了使用 unix_to_data() 方法的实例：
```python
print(unix_to_data(1588590928))
```
以上实例运行后输出结果为：
```python 
2020-5-4
```