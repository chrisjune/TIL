# varnish setting
## Install varnish
* linux의 경우, sudo apt-get install varnish로 쉽게 설치
* macOs, windows의 경우, 컴파일 패키지들을 설치후 소스를 받아서 빌드하여 설치
## Configure
* 필수. `/etc/varnish/default.vcl` - varnish에서 캐쉬할 서버정보 입력
1. vi /etc/varnish/default.vcl
2. 내용추가
```
backend default {
    .host = "{YOUR_DOMAIN or IP_ADDRESS}";
    .port = "{YOUR SERVER PORT}";
}
```
* 옵션. `/etc/default/varnish` - varnish에서 서빙할 포트등의 정보 수정
1. vi /etc/default/varnish
2. 내용 수정
```
DAEMON_OPTS="-a :{PORT_NUBMER_WHAT_YOU_WANT_TO_SERVE} \
             -T localhost:6082 \
             -f /etc/varnish/default.vcl \
             -S /etc/varnish/secret \
             -s malloc,256m"
```
## 명령어
* service varnish start  - varnish 시작
* service varnish stop - varnish 종료
* service varnishlog  - varnish log display
* service varnishtop - varnish log entry ranking
* service varnishhist - varnish request histogram
* service varnishstat - varnish cache statistics
## 참고링크
* https://varnish-cache.org/docs/trunk/tutorial/index.html

