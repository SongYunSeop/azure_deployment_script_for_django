# Azure WebApp Deployment Script for Django

Azure WebApp에 Django 프로젝트를 배포할 때 필요한 파일들 입니다.


## File List

- .deployment
- deploy.cmd
- runtime.txt
- web.x.x.config
- ptvs_virtualenv_proxy.py

## .deployment

배포 시 실행할 파일을 명시해줍니다.

`azure-cli`로 생성가능함

## deploy.cmd

배포 시 실행하는 스크립트

`azure-cli`로 생성가능함

## runtime.txt

프로젝트에서 사용하는 Python 버젼을 알려줍니다.

Python2.7 버전을 사용하면 아래처럼 적고,

```
python-2.7
```

Python3.x 버젼을 사용하면 아래와 같이 적습니다.

```
python-3.4
```

## web.x.x.config

웹 서버의 설정들이 있는 파일입니다.

파일의 10번 줄에 `{project_name}`을 사용하는 장고 프로젝트 이름으로 바꿔줍니다.

장고 프로젝트 이름이 `djangogirlsdaejeon`이라면 아래처럼 바꾸면 됩니다.

```
...
    <add key="DJANGO_SETTINGS_MODULE" value="djangogirlsdaejeon.settings" />
...
```

## ptvs_virtualenv_proxy.py

가상환경 프록시를 구성해주는 파일입니다.

## References

- https://docs.microsoft.com/ko-kr/azure/app-service-web/web-sites-python-configure
