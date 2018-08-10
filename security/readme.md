# javascript
location.href = xxxx
这里xxxx如果是javascript：alert()  就存在漏洞，需要正则确认格式
/^(http(s)?:)?\/\//i.test(url)
