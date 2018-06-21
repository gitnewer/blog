## cookie生成

## cookie删除
删除cookie的时候，需要有效期，域和路径都有
跨域不能删除cookie
浏览器删除成功的cookie是在开发者工具看不到的

## cookie实现
谷歌浏览器标记1969年的cookie是浏览器对session过期时间的cookie的一种实现
document.cookie = "cccc=dcsaf"
document.cookie = "cccc=dcsaf; expires=Thu, 22 May 2018 02:32:33 GMT; path=/; domain=aaa.com"
