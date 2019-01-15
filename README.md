import requests


# url赋值
url = 'https://item.jd.com/12576741741.html'
# try except语句
try:
    # 用request获取地址信息
    r = requests.get(url)
    # raise方法获取状态码
    r.raise_for_status()
    # 获取url内容的编码信息
    r.encoding = r.apparent_encoding
    # 打印url，从0-1000
    print(r.text[:1000])
except:
    # 或者报错为失败
    print('失败')
