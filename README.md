#### 说明

Alpine:v3.4 + Selenium +Firefox

#### 创建镜像

```
$ docker build -t="leafney/alpine-selenium-firefox" .
```

#### 创建一个容器进行测试

```
$ docker run -it --name alseff leafney/alpine-selenium-firefox /bin/sh
```

#### 拷贝 py 文件到容器中

```
$ docker cp firefox.py alseff:/root
```

#### Size

leafney/alpine-selenium-firefox   latest   251.3 MB

***

#### Selenium + Firefox Demo

```
# coding:utf-8

import time
from selenium import webdriver
from pyvirtualdisplay import Display

display = Display(visible=0, size=(800, 800))
display.start()

driver = webdriver.Firefox()
driver.get('http://www.cnblogs.com/')

time.sleep(5)
title = driver.title
print(title.encode('utf-8'))

# html=driver.page_source
# print(html)

# Release memory
driver.close()
driver.quit()
display.stop()
```
