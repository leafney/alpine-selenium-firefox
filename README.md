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

