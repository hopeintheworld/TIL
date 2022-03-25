# Middleware
* body-parser
  * Third-Party Middleware
  * 사용자가 전송한 Post 정보를 내부적으로 분석하여 정의한 callback을 호출하도록 한다.
  * body-parser의 결과물이 request.body에 저장되고 body data를 사용할 수 있다.

* compression
  * HTTP 파일 데이터 압축 middleware.

# Middleware 만들기
* app.use('path', function(req, res, next) {
*   something();
*   next(); -> 다음 middleware 실행.
* });

* use 대신 get/post 등을 사용해서 방식에 따라 호출을 막을 수 있다.

# Middleware 실행순서
* Application-level middleware
  * next('route'); -> 다음 route의 middleware 실행.
  * next(); -> 현재 route의 middleware 실행.

# 정적파일 접근
* app.use(express.static('path'));
