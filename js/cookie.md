## cookie生成

document.cookie = "cccc=dcsaf"
document.cookie = "cccc=dcsaf; expires=Thu, 22 May 2018 02:32:33 GMT; path=/; domain=aaa.com"

## cookie删除
删除cookie的时候，需要有效期，域和路径都有
跨域不能删除cookie
浏览器删除成功的cookie是在开发者工具看不到的

## cookie实现
谷歌浏览器标记1969年的cookie是浏览器对session过期时间的cookie的一种实现

session cookie 火狐会显示“会话”

如果document.cookie = "cccc=dcsaf"
火狐会按照根域名的会话cookie写入
chrome会按照子域名，页面地址的path写入
