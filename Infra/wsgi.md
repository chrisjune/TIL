# Django - Uwsgi - Nginx
## wsgi
* wsgi는 웹서버 게이트웨이 인터페이스, 웹서버와 웹앰의 통신방식의 인터페이스를 의미
* PEP333, 3333에서 제안되었고 이후 여러 프로젝트로구현됨
* 과거 CGI, FastCGI등과 같은 API중에서 사용해야했지만, WSGI는 저수준으로 만들어 
* 프레임워크간 벽을 허물었다.
## uWsgi
* WSGI 컨테이너로서, WSGI어플리케이션션을 담아서 실행하는 주체
* uWSGI가 웹서버와 소통할 수 있도록 설정
* Flask, Django는 이미 WSGI 표준을 따르고 있기 때문에 바로 웹서버에 연결해 사용할 수 있다.
 
