# HTML의 기본구성

- HTML(Hypertext Markup Language)은 컨텐츠의 구조를 정의하는 마크업 언어로, 컨텐츠(내용)에 태그(마크)를 씌워 구조를 구분하여 정의
    - 시작 태그(Start tag)와 종료 태그(End tag), 컨텐츠(Contents)로 구성
        
        ```html
        <시작태그>컨텐츠</종료태그>
        ```
        
    - **시작 태그는 `<>`로 감싸 내용의 시작을 표시**하고, **종료 태그는 `</>`로 감싸 내용의 끝을 표시**
        
        ```html
        <제목>바로 실행해보면서 배우는 HTML5/CSS3</제목>
        <부제목>쉽고 빠르게 배우는 HTML5와 CSS3</부제목>
        <내용>HTML5와 CSS3의 필수 개념과 실습까지</내용>
        ```
        
    - 제목, 부제목, 내용은 각각 **`<h1>`, `<h2>`, `<p>` 태그를 사용**
        
        ```html
        <h1>바로 실행해보면서 배우는 HTML5/CSS3</h1>
        <h2>쉽고 빠르게 배우는 HTML5와 CSS3</h2>
        <p>HTML5와 CSS3의 필수 개념과 실습까지</p>
        ```
        

---

# 기본적인 HTML 문서 구조

- HTML문서는 요소만으로 완성할 수 없다
    
    ```html
    <!DOCTYPE html>
    <html lang="ko">
    <head>
    <meta charset="utf-8">
    <title>구름EDU</title>
    </head>
    <body>
    <h1>바로 실행해보면서 배우는 HTML/CSS</h1>
    <p>HTML과 CSS에 대해서 배워봅시다!</p>
    </body>
    </html>
    ```
    
    1. `<!DOCTYPE html>`
        - 문서 형식(Document type)을 정의할 때 사용하는 문장
    2. `<html lang="ko">`
        - 페이지의 주 언어가 한국어라는것을 명시

---

# Head와 Body

- `<html>`태그 안에는 크게 **`<head>`태그와 `<body>`태그가 존재,각 태그 안에 여러 가지 태그를 배치하여 문서를 구성**
    
![](https://velog.velcdn.com/images/hyeon_17/post/074d4957-adc1-4b48-8644-40a45e140414/image.png)

    
    ```html
    <!DOCTYPE html>
    <html lang="ko">
    <head>
    <meta charset="utf-8">
    <title>구름EDU</title>
    </head>
    <body>
    <h1>한 눈에 끝내는 HTML5/CSS3</h1>
    <p>HTML과 CSS에 대해서 배워봅시다!</p>
    </body>
    </html>
    ```
    

### <head> 태그

- **`<head>` 태그**는 HTML 문서에 대한 정보를 담고 있는데, 일반 사용자는 웹 사이트에서 `<head>`태그에 속한 정보를 볼 수 없다.
    - `<meta>` : **문서와 관련된 정보를 담는 태그**
    - `<title>`: **웹 페이지의 제목을 담는 태그**

### <body> 태그

- **`<body>` 태그**는 HTML 문서 중 사용자에게 실제로 보여지는 부분
    - `<h1>` : **제목을 표시하는 태그**
    - `<p>` : **단락을 표시하는 태그**
- **`<head>` 태그 내부와 `<body>` 태그 내부에 존재하는 태그는 종류에 상관 없이 여러 번 사용가능**

---

# **기본적인 레이아웃**

- **시맨틱 태그(Semantic tag)**
    - **`<header>`**: 웹 페이지 혹은 `<section>`의 소개나 제목을 담기 위해 사용하는 요소입니다.
    - **`<nav>`**: 내비게이션 역할을 수행하는 요소로, 페이지 이동을 위한 메뉴를 주로 담습니다.
    - **`<section>`**: 기준에 따라 구획을 구분하기 위해 사용하는 요소입니다. 기준에 맞는 `<article>`들을 담습니다.
    - **`<article>`**: 주 내용을 담기 위해 사용하는 요소입니다.
    - **`<aside>`**: 광고 또는 사이트의 주변 부분에 해당하는 내용을 담기 위해 사용하는 요소입니다.
    - **`<footer>`**: 일반적으로 웹 사이트의 가장 아래에 들어가는 회사 정보나 사이트 정보 등의 추가 정보를 담기 위해 사용하는 요소입니다.

---

# **제목과 본문 태그**

- **제목 태그(Heading tag)**는 제목을 나타내고 싶을 때 사용
- 중요도에 따라 `<h1>`부터 `<h6>`까지 사용
    - 컨텐츠의 대제목이 `<h1>`에 해당하고, 소제목 혹은 부제목이 `<h2>`나 `<h3>`에 해당
        
        ```html
        <h1>h1 제목입니다.</h1>
        <h2>h2 제목입니다.</h2>
        <h3>h3 제목입니다.</h3>
        <h4>h4 제목입니다.</h4>
        <h5>h5 제목입니다.</h5>
        <h6>h6 제목입니다.</h6>
        ```
        

### **본문 태그**

- `<p>`: paragraphs의 약자로, **단락**혹은 **문단**이라는 뜻
    
    ```html
    <p>구름IDE는 언제 어디서나
    	개발할 수 있는 웹 기반 IDE입니다.
    	동일한 도커 컨테이너 환경에 접속한
    	모든 사용자들은 코드를 동시 편집할 수 있고,
    	공유 링크를 통해 협업과 질문을
    	매우 편리하게 진행할 수 있습니다.</p>
    ```
    
- `<div>`: division의 약자로 **분할**의 뜻
    
    ```html
    <section>
    	<div>
    		<p>1번 문장입니다.</p>
    		<p>2번 문장입니다.</p>
    	</div>
    	<p>3번 문장입니다.</p>
    </section>
    ```
    
- `<pre>`: preformatted의 약자로, **형식화된 텍스트**를 브라우저에 그대로 표시
    
    ```html
    <pre>구름IDE는 언제 어디서나
    	개발할 수 있는 웹 기반 IDE입니다.
    	동일한 도커 컨테이너 환경에 접속한
    	모든 사용자들은 코드를 동시 편집할 수 있고,
    	공유 링크를 통해 협업과 질문을
    	매우 편리하게 진행할 수 있습니다.</pre>
    ```
    
- `<br>`: break의 약자로, 엔터(enter)와 동일한 역할, 즉 **줄 바꿈**을 수행
    
    ```html
    <p>구름IDE는 언제 어디서나<br>
    	개발할 수 있는 웹 기반 IDE입니다.<br>
    	동일한 도커 컨테이너 환경에 접속한<br>
    	모든 사용자들은 코드를 동시 편집할 수 있고,<br>
    	공유 링크를 통해 협업과 질문을<br>
    	매우 편리하게 진행할 수 있습니다.</p>
    ```
    
  ![](https://velog.velcdn.com/images/hyeon_17/post/6c51d06a-4615-4129-8705-72fa0a822d74/image.png)

    - `<br>`태그와 같이 종료 태그를 쓰지 않는 요소를 **빈 요소(Empty element)**라고 부른다.

---

# **글자와 관련된 태그**

### **`<strong>, <em>` 태그**

- 해당 컨텐츠가 **중요하다**는 것을 강조하기 위해 사용
    - `<strong>`: 태그로 감싼 단어 혹은 문장을 **볼드체**로 바꿈
    - `<em>`: emphasized의 약자이며, 태그로 감싼 단어 혹은 문장을 **이탤릭체**로 바꿈

### **`<sub>, <sup>` 태그**

- `<sub>`: 태그로 감싼 단어 혹은 문장을 **일반 위치**보다 **아래로** 내림
- `<sup>`: 태그로 감싼 단어 혹은 문장을 **일반 위치**보다 **위로** 올림

### **`<ins>, <del>` 태그**

- `<ins>`: 태그로 감싼 단어 혹은 **문장 아래 밑줄**을 추가
- `<del>`: **취소선**을 추가

---

# **링크 태그**

- 하이퍼 링크(Hyperlink)는 하이퍼 텍스트를 가능하게 만든 핵심 도구

### **링크 태그 `<a>`**

- `<a>`는 **anchor(닻)**의 약자로, HTML에서 **하이퍼 링크의 역할을 수행**
- `<a>`태그를 사용하면 링크를 통해 다른 웹페이지로 이동하거나 문서로 이동할 수 있는 통로가 마련
    
  ![](https://velog.velcdn.com/images/hyeon_17/post/9920ed03-4c6d-4a49-9e03-bf729843aeab/image.png)


    

### **`<a> 태그의 구성`**

- **속성(attributes)은 태그의 특징, 즉 태그에 대한 추가 정보의 모음**
- **링크 주소라는 종류는 키(Key)**, 그에 따른 실제 **링크 주소는 값(Value)**
    - 값은 큰따옴표("") 또는 작은따옴표('') 처리
- 만약 태그가 여러 개의 속성을 갖고 있는 경우 띄어쓰기로 구분

---

# **링크 태그의 속성**

### **`<a>`의 속성, href**

- **href**는 **Hypertext Reference**의 약자로, `<a>`가 참조하는 **웹 사이트 주소(경로)**를 값으로 가집니다
- `<a>` 태그에서는 **`a` 다음에 공백을 입력**한 뒤 **`href`와 웹 페이지 주소 및 경로를 입력**

```html
<a href="https://ide.goorm.io">구름IDE</a>
```

### **`<a>`의 속성, target**

- `target`속성은 링크를 클릭했을 때 **해당 페이지를 어디에서 열지 정하는 속성**
- `target`속성에서 사용할 수 있는 대표 값
    - **`_self`는 현재 탭에서 링크를 열음**
    - **`_blank`는 새 탭 혹은 새 창(옛 버젼 브라우저의 경우)에서 링크를 열음**
    
    ```html
    <a href="https://ide.goorm.io" target="_self">구름IDE</a>
    <a href="https://edu.goorm.io" target="_blank">구름EDU</a>
    ```
    

---

# **웹사이트의 경로와 주소**

- **출발지부터 목적지까지 가는 길** 모두를 통틀어 **경로(Path)라고 한다.**
    
   ![](https://velog.velcdn.com/images/hyeon_17/post/41853dd7-04ed-464f-830c-0358b6305000/image.png)

    

### **URL**

- 웹 사이트 주소(도메인, domain)와 경로(path)를 합쳐 **URL(Uniform Resource Locator)**이 생성
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/a3687c0a-8e6e-41c1-893f-70338930fcf6/image.png)   
- HTML 페이지, CSS 문서, 이미지 등을 **자원(Resource)**이라고 부르며, **URL**은 인터넷에서 자원의 위치를 표현
- **절대 URL(Absolute URL):** 접근하는 **최초 시작점(주소)부터 경유한 경로를 모두 기록**하여 리소스의 위치를 나타냅니다.
- **상대 URL(Relative URL):** **현재 위치(기준점)를 기준으로 상대적인 경로를 기록**하여 리소스의 위치를 나타냅니다.
- 예시
    
    ```html
    절대 URL : [https://edu.goorm.io/lecture/바로-실행해보면서-배우는.html](https://edu.goorm.io/lecture/%EB%B0%94%EB%A1%9C-%EC%8B%A4%ED%96%89%ED%95%B4%EB%B3%B4%EB%A9%B4%EC%84%9C-%EB%B0%B0%EC%9A%B0%EB%8A%94.html)
    상대 URL : lecture/바로-실행해보면서-배우는.html
    ```
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/ce0f52c1-ef17-4d28-aad9-6f8e5b300449/image.png)

    
    ```html
    절대 URL : https://edu.goorm.io/lecture/바로-실행해보면서-배우는.html
    상대 URL : 바로-실행해보면서-배우는.html
    ```
    
   ![](https://velog.velcdn.com/images/hyeon_17/post/01c73715-fa11-49e8-95c7-d58cf915b009/image.png)

    

---

# **이미지 태그**

### **`<img>` 사용법과 속성**

- **`<img>`:** 이미지 태그는 **넣고자 하는 이미지에 대한 속성을 필히 작성해야 하는 태그,종료 태그를 작성하지 않는다.**
    
    ```html
    <img src="이미지 url"/>
    ```
    
- `src:` **source**의 약자로 근원이라는 뜻, **불러올 이미지의 파일 경로 또는 URL을 속성값**으로 가집니다.
- `alt:` **Alternative text**의 약자로 **대체 문구**라는 뜻을 가집니다. 말 그대로 이미지가 정상 출력되지 않거나 이미지 파일이 아예 존재하지 않는 경우, **이미지 대신 표시할 문구를 값으로**가집니다.
    
    ```html
    <img src="이미지 URL" alt="이미지 대체 문구"/>
    ```
    

### **이미지 크기 조정**

- `<img>`태그에서 **이미지의 높이나 너비를 지정하는 속성** 또한 추가할 수 있다.
    
    ```html
    <img src="[https://t1.daumcdn.net/thumb/R720x0/?fname=http://t1.daumcdn.net/brunch/service/user/QsT/image/NSTeOeMe0MddpqlJ23FZV7hJGvg](https://t1.daumcdn.net/thumb/R720x0/?fname=http://t1.daumcdn.net/brunch/service/user/QsT/image/NSTeOeMe0MddpqlJ23FZV7hJGvg)" alt="dog's photo" width="430px" height="320px"/>
    ```
    
    - 권장 사항은 아님, **HTML은 웹 페이지의 구조를 정의**할 때, **CSS는 웹 페이지와 관련된 모든 스타일을 정의**할 때 사용

---

# **오디오와 비디오 태그**

### **오디오 태그**

- **오디오 파일이 저장된 경로를 `src`(source) 값으로 설정**하면, 웹 페이지에 해당 오디오 파일을 재생하는 플레이어가 추가
- 확장자의 음원 형식을 뜻하는 `type`속성은 생략할 수 있다.
    
    ```html
    <audio controls>
      <source src="assets/audio/dance.mp3" type="audio/mpeg">
    </audio>
    ```
    

### **비디오 태그**

- **비디오 파일이 저장된 경로를 `src`(source) 값으로 설정**하면, 해당 비디오 파일을 재생할 수 있는 플레이어가 웹 페이지에 추가
- `video>`태그에서  `type`속성을 생략할 수 있다.
    
    ```html
    <video controls>
       <source src="assets/video/dance.mp4" type="video/mp4">
    </video>
    ```
    
- `<video>`태그는 `audio>`태그와 다르게 `height`와 `width`속성을 지정할 수 있다.
    
    ```html
    <video width="640" height="360" controls>
       <source src="assets/video/dance.mp4" type="video/mp4">
    </video>
    ```
    

---

# **유튜브 영상 삽입**

- 유튜브 영상 아래에 공유하기를 클릭
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/7c06ba6d-5d89-4a96-bf6d-efab158a3e76/image.png)

    
- 공유창이 뜨면 HTML 코드를 제공하는 `< >퍼가기`를 클릭
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/25f016fe-f456-4f66-8acb-64decee60f5c/image.png)

    
- 동영상 퍼갈 수 있는 HTML 소스 코드가 뜨면 이를 복사하여 아래와 같이 붙여넣기
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/888fe849-6850-4004-bfa0-7d81a022e46c/image.png)

    
    ```html
    <iframe width="560" height="315" src="https://www.youtube.com/embed/WnumLT3ZcLY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    ```
    
    - `src`의 속성 값인 URL을 살펴보면, `/embed/`뒤에 영어와 숫자를 조합한 Youtube 영상 ID를 볼 수 있다. 이 영상 ID는 모든 유튜브 영상의 주소 URL을 보면 찾을 수 있으며, 이 영상 ID를 바꿔줌으로써 원하는 영상으로 변경할 수 있다.
- 유튜브 영상을 추가할 때 쓰는 `<iframe>`태그는 유튜브 영상 뿐만 아니라 웹 페이지를 삽입할 때도 사용
    
    ```html
    <iframe src="https://www.youtube.com/embed/WnumLT3ZcLY"></iframe>
    ```
    

---

# **form 태그**

- **`<form>` 태그는 하나의 신청서 종이**
    
    ```html
    <form>
        <!--다양한 input form이 들어감-->
    </form>
    ```
    
    - `<form>`태그로 묶으면 그 안에는 **질문, 선택사항, 답변 작성 공간 등이 배치**

### **form 태그의 다양한 속성**

```html
<form action='http://server.me/check' method="get">
    <!--다양한 input form이 들어감-->
</form>
```

- `action`속성은 데이터를 보낼 URL을 지정
- `method`속성은 보내는 방식을 지정
    - `get`또는 `post`를 값으로 가지며, GET 방식과 POST 방식의 기능은 동일
    - 두 기능 모두 브라우저에서 사용자가 양식에 입력한 데이터를 서버로 보내는 역할을 수행
        
       ![](https://velog.velcdn.com/images/hyeon_17/post/7b27a0f7-ed08-4039-8ec9-f73ed8ee74d9/image.png)

        

### **GET과 POST**

- 사용자가 서버로 데이터를 전송할 때 데이터는 **HTTP Request Message라는 특별한 메세지에 담겨 보내진다.**
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/1c11c848-3f1c-4297-9504-84cfce761f18/image.png)

- 메세지는 크게 **Header**와 **Body**두 부분으로 나뉜다.
    
   ![](https://velog.velcdn.com/images/hyeon_17/post/1f3c8bd0-f1d9-47ae-a66c-0d9bea277eb8/image.png)

    
- 메세지의 Header에는 데이터의 목적지가 되는 **서버의 URL**이 작성
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/e90432cc-5849-4177-b1a2-ac3863d2dc5f/image.png)

    
- **GET 방식**의 경우 사용자가 입력한 **데이터를 서버URL 말미에 이어 붙여 숨김 없이 보낸다.**
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/46045a2b-ff32-42dd-a5be-43fffdbfe592/image.png)

    
- **POST 방식**은 데이터를 URL 끝에 붙이지 않고 데이터의 내용을 메세지의 **Body 부분**에 숨겨 보낸다.
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/6419df76-ce10-4aa1-a894-5506dfecb27d/image.png)

    
    ```html
    https://ide.goorm.io?id=goorm&pw=asd123
    ```
    
- POST 방식은 받는 서버 주소에 데이터를 적지 않고 편지 봉투 내부, 즉 메세지의 Body에 숨겨 보낸다.
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/57d35dfb-109d-4d90-82bc-a6f36fca44e3/image.png)


### **GET과 POST를 따로 사용하는 이유**

- GET 방식은 **get**이란 말 그대로 '**받다**'라는 뜻으로, 주로 **서버에 데이터를 요청하고 데이터를 받아오는 역할을 수행, 데이터 조회**를 목적으로 사용
    - 예시: 검색
        - 검색 창에 검색을 해보면 주소창에 사용자가 검색한 검색어가 그대로 노출된다. 만약 주소창에 적힌 검색어를 바꾸어 접속하면 바뀐 검색어로 검색된 결과가 노출
            
            ![](https://velog.velcdn.com/images/hyeon_17/post/c4a537cd-8803-4cd7-80ff-fcdb4fc442d2/image.png)

            
- POST 방식은 **post**란 말 그대로 '**게시하다**'는 뜻을 가지며 서버에 있는 **데이터를 쓰거나 수정, 삭제**할 때 주로 사용
    - 예시: 게시물 작성
        - 게시물 작성, 수정 혹은 삭제가 GET으로 이루어진다면 의도치않게 주소만으로 게시물이 삭제가 되거나, 본인의 것이 아닌 계정으로 로그인을 하는 등의 문제가 발생할 수 있다. 따라서 로그인이나 게시물 작성, 회원가입 등 데이터에 대한 보안이 필요한 경우 POST 방식을 이용
            
            ![](https://velog.velcdn.com/images/hyeon_17/post/2f0e0c9e-9d6c-48be-8c48-198a298048e7/image.png)

    

---

# **input 태그**

- `<input>`태그는 입력 양식 태그 중에서도 가장 중요하고 많이 쓰이는 태그. 주로 **사용자에게 입력을 받기 위해 사용**되며, **빈 태그**이기 때문에 종료 태그를 사용하지 않는다.
    - 제출 버튼, 파일 업로드, 날짜 등 매우 다양한 값이 입력
    - `type`이라는 속성을 설정하여 어떤 값을 입력할 것인지 결정
        - 일반 텍스트와 이메일 주소, 비밀번호 등 문자로 이루어진 값을 입력
            
            ```html
            <h3>text</h3>
            <input type="text" name="myname">
            <hr>
            
            <h3>email</h3>
            <input type="email" name="email">
            <hr>
            
            <h3>password</h3>
            <input type="password" name="pw">
            <hr>
            ```
            
        - 버튼, 체크박스 등 형식을 입력
            
            ```html
            <h3>button</h3>
            <input type="button" value="Button">
            <hr>
            
            <h3>search</h3>
            <input type="search" name="search">
            <hr>
            
            <h3>checkbox</h3>
            <input type="checkbox" name="python" value="python" checked>Python<br>
            <input type="checkbox" name="javascript" value="javascript">Javascript<br>
            <input type="checkbox" name="cpp" value="cpp">C++<br>
            <hr>
            
            <h3>file</h3>
            <input type="file" name="myfile">
            <hr>
            
            <h3>radio</h3>
            <input type="radio" name="gender" value="male" checked> 남자<br>
            <input type="radio" name="gender" value="female"> 여자<br>
            <hr>
            ```
            
        - 그 외 다양한 값을 입력
            
            ```html
            <h3>color</h3>
            <input type="color" name="color">
            <hr>
            
            <h3>date</h3>
            <input type="date" name="birthday">
            <hr>
            
            <h3>number</h3>
            <input type="number" name="quantity" min="1" max="10" step="1" value="1">
            <hr>
            
            <h3>range</h3>
            <input type="range" name="points" min="0" max="10" step="1" value="5">
            <hr>
            
            <h3>reset</h3>
            <input type="reset">
            <hr>
            
            <h3>time</h3>
            <input type="time" name="mytime">
            <hr>
            ```
            
    - 입력 받은 데이터를 구분하기 위해 **`name` 속성을 키(key)로, 입력 받은 데이터를 값(value)으로 전송**
        - `type="password"`는 `text`와 다르게 입력 칸에 값을 입력하면 별표로 표시되어 노출되지 않음
            - placeholder: **가이드 문구를 지정하는데 사용하는 속성**
            
            ```html
            <h3>회원가입</h3>
            <form action="my-app" method="get">
              <input type="text" name="id" placeholder="아이디를 입력하세요.">
              <input type="password" name="password" placeholder="비밀번호를 입력하세요.">
            </form>
            ```
            
- `<label>`태그는 입력 양식의 역할이 무엇인지 알려주는 이름표 역할을 수행
    - `<label>`태그에 해당하는 이름표를 클릭하면 입력 칸이 활성화
        
        ![https://grm-project-template-bucket.s3.ap-northeast-2.amazonaws.com/lesson/les_NabiQ_1635225418558/b3a320d09786056830de4d352b258edc1bcef283c6f824c36d06e8ec4c2d464f.gif](https://grm-project-template-bucket.s3.ap-northeast-2.amazonaws.com/lesson/les_NabiQ_1635225418558/b3a320d09786056830de4d352b258edc1bcef283c6f824c36d06e8ec4c2d464f.gif)
        
        ```html
        <h3>회원가입</h3>
        <form action="my-app" method="get">
          <div>
            <label for="userid">아이디: </label>
            <input type="text" id="userid" name="id" placeholder="아이디를 입력하세요.">
          </div>
          <div>
            <label for="password">비밀번호: </label>
            <input type="password" id="password" name="password" placeholder="비밀번호를 입력하세요.">
          </div>
        </form>
        ```
        

---

# **select 태그**

- 선택 박스를 배치하기 위해서는 `<select>`태그를 사용하며, `<select>`태그는 `<option>`태그로 이루어져 있는 각 선택지를 하나로 감싸는 역할을 수행
    - `select>`태그는 `name`이라는 속성을, `<option>`태그는 `value`라는 속성을 필히 가져야한다. 여기서 `name`속성은 `<input>`태그의 `name`속성과 동일한 역할을 수행. `<input>`태그에서는 한 태그 안에 있는 `name`과 `value`가 짝이었지만, `<select>`태그에서는 `<select>`태그의 `name`과 `<option>`태그의 `value`가 서로 짝을 이룬다.
        
        ```html
        <select name="job" id="job">
          <option value="student">학생</option>
          <option value="teacher">선생님</option>
          <option value="etc">기타</option>
        </select>
        ```
        

---

# **textarea 태그**

- `<textarea>`태그는 `rows`, `cols`속성과 사용할 수 있는데, 값으로 숫자를 넣으면 `<textarea>`의 크기를 조정할 수 있습니다. 정확히 말하자면 `cols`는 글자 수 만큼, `rows`는 글 줄 수 만큼 조정
- `<textarea>`태그는 빈 요소가 아니기 때문에 종료 태그가 존재
    - 요소 안에 내용을 작성한다면  `value`속성과 동일하게 사라지지 않는 값으로 처리됨
    - 예시
        
        ```html
        <h3>회원가입</h3>
        <form action="my-app" method="get">
        	<div>
        		<label for="userid">아이디: </label>
        		<input type="text" id="userid" name="id" placeholder="아이디를 입력하세요.">
        	</div>
        	<div>
        		<label for="password">비밀번호: </label>
        		<input type="password" id="password" name="password" placeholder="비밀번호를 입력하세요.">
        	</div>
        	<div>
        		<label for="gender">성별: </label>
        		<select name="gender" id="gender">
        			<option value="male">남성</option>
        			<option value="female">여성</option>
        		</select>
        	</div>
        	<div>
        		<label for="job">직업: </label>
        		<select name="job" id="job">
        			<option value="student">학생</option>
        			<option value="teacher">선생님</option>
        			<option value="etc">기타</option>
        		</select>
        	</div>
        	<div>
        		<label for="introduce">자기소개: </label>
        		<textarea name="introduce" id="introduce" placeholder="자기소개를 입력하세요" cols="20" rows="6"></textarea>
        	</div>
        </form>
        ```
        

---

# **button 태그**

- `<button>`태그는 **HTML 요소를 `<button>` 태그 내부에 담아 사용할 수 있다는 장점**
    - 예시
        
        ```html
        <h3>회원가입</h3>
        <form action="my-app" method="get">
        	<div>
        		<label for="userid">아이디: </label>
        		<input type="text" id="userid" name="id" placeholder="아이디를 입력하세요.">
        	</div>
        	<div>
        		<label for="password">비밀번호: </label>
        		<input type="password" id="password" name="password" placeholder="비밀번호를 입력하세요.">
        	</div>
        	<div>
        		<label for="gender">성별: </label>
        		<select name="gender" id="gender">
        			<option value="male">남성</option>
        			<option value="female">여성</option>
        		</select>
        	</div>
        	<div>
        		<label for="job">직업: </label>
        		<select name="job" id="job">
        			<option value="student">학생</option>
        			<option value="teacher">선생님</option>
        			<option value="etc">기타</option>
        		</select>
        	</div>
        	<div>
        		<label for="introduce">자기소개: </label>
        		<textarea name="introduce" id="introduce" placeholder="자기소개를 입력하세요" cols="20" rows="6"></textarea>
        	</div>
        	<button type="submit">제출</button>
        </form>
        ```
        
    - `type="reset"`도 사용할 수 있는데, 이는 **입력 양식을 모두 초기화하는 역할을 수행**
        
        ![https://grm-project-template-bucket.s3.ap-northeast-2.amazonaws.com/lesson/les_xnUOI_1635225418593/c94abe070cbd83d3ce346970b062dcbe1f45114a8d97fc9e282d0c89fed71841.gif](https://grm-project-template-bucket.s3.ap-northeast-2.amazonaws.com/lesson/les_xnUOI_1635225418593/c94abe070cbd83d3ce346970b062dcbe1f45114a8d97fc9e282d0c89fed71841.gif)
        
        ```html
        <input type="reset">
        ```
        

---

# **표(Table)**

### **테이블의 구조**

- 표의 일반적인 구성
    - 전체를 담고 있는 테이블
    - 데이터를 담은 데이터 셀
    - 각 열의 제목을 담은 제목 셀
    - 각 행
    
   ![](https://velog.velcdn.com/images/hyeon_17/post/8f989217-67f8-4acf-ab5f-c51bccb3e667/image.png)

    
- HTML 코드로 바꾼 경우
    
    ![](https://velog.velcdn.com/images/hyeon_17/post/59878dc9-419e-4196-8c39-9ec88a39c805/image.png)

    
    ```html
    <table> <!--전체를 담고 있는 표-->
    	<tr> <!--각 행-->
    		<th>나이</th> <!--각 열의 제목을 담은 제목 셀-->
    		<th>직업</th>
    		<th>이름</th>
    	</tr>
    	<tr>
    		<td>23</td> <!--데이터를 담은 데이터 셀-->
    		<td>대학생</td>
    		<td>김구름</td>
    	</tr>
    	<tr>
    		<td>24</td>
    		<td>직장인</td>
    		<td>구우름</td>
    	</tr>
    </table>
    ```
    
- `<th>`, `<td>`, `<tr>`은 각각 **table heading**, **table data**, **table row**를 축약한 태그
- 왼쪽에 표 제목이 있는 표
    
   ![](https://velog.velcdn.com/images/hyeon_17/post/5e6bf265-a438-4d75-acfe-a8b35dcbd9d7/image.png)

    
    ```html
    <table>
    	<tr>
    		<th>나이</th>
    		<td>23</td>
    		<td>24</td>
    	</tr>
    	<tr>
    		<th>직업</th>
    		<td>대학생</td>
    		<td>직장인</td>
    	</tr>
    	<tr>
    		<th>이름</th>
    		<td>김구름</td>
    		<td>구우름</td>
    	</tr>
    </table>
    ```
    
    - 행(`<tr>`)을 기준으로 테이블 태그를 작성해야 조금 편하게 작성할 수 있다.

### **테이블 태그의 속성**

- `colspan="숫자"`는 `"숫자`"만큼 셀이 행을 점유
- `rowspan="숫자"`는 `"숫자"`만큼 셀이 열을 점유
    
    ```html
    <table>
    	<tr>
    		<th>나이</th>
    		<td>23</td>
    		<td>24</td>
    	</tr>
    	<tr>
    		<th>직업</th>
    		<td colspan="2">대학생</td>
    	</tr>
    	<tr>
    		<th>이름</th>
    		<td>김구름</td>
    		<td>구우름</td>
    	</tr>
    </table>
    ```
    
    - `colspan`속성을 이용하여 직업 행에 위치한 '대학생'이라는 두 개의 셀이 병합. 만약 그렇게 보이지 않는다면 이는 **셀 테두리가 없고 좌측으로 글씨가 정렬**되었기 때문. 실제로는 **두 셀이 병합되어 있다는 점 참고**

---

# **목록(List)**

- 목록(List)은 크게 순서 없는 목록(Unordered List)과 순서 있는 목록(Ordered List)로 나뉜다.

### **순서 없는 목록**

- **`<ul>` : unordered list**의 약자, **리스트의 항목을 감싸는 태그**
- **`<li>`는: list item**의 약자, **리스트에 나열할 항목을 담아두는 태그**
- 예시
    - 학교 과제하기
    - Python 강의 듣기
    
    ```html
    <ul>
    	<li>학교 과제하기</li>
    	<li>Python 강의 듣기</li>
    </ul>
    ```
    

### **순서 있는 목록**

- 다음 세 가지 요소를 순서 있는 목록으로 코드를 작성
    1. 세제
    2. 돼지 고기 300g
    3. 생수
    
    ```html
    <ol>
    	<li>세제</li>
    	<li>돼지 고기 300g</li>
    	<li>생수</li>
    </ol>
    ```
    

### **중첩 리스트**

- 리스트 태그는 들여쓰기가 기본적인 스타일. 중첩을 반복하여 한 번 더 들여쓰기하면 한 번 더 하위 항목으로 들어간다.
    
    ```html
    <h3>오늘 할 일</h3>
    <ul>
    	<li>학교 과제하기
    		<ol>
    			<li>물리학 실험 보고서</li>
    			<li>확률과 통계 chapter.3 풀이</li>
    		</ol>
    	</li>
    	<li>Python 강의 듣기</li>
    </ul>
    <h3>장바구니</h3>
    <ol>
    	<li>세제</li>
    	<li>돼지 고기 300g</li>
    	<li>생수</li>
    </ol>
    ```
    

---

# **목록 태그의 속성**

### **`<ol>` 태그 속성**

- `start="숫자"`는 리스트가 시작하는 숫자를 정합니다.
    
    ```html
    <ol start="4">	
    	<li>세제</li>
    	<li>돼지 고기 300g</li>
    	<li>생수</li>
    </ol>
    ```
    
- `type="문자"`는 순서를 시작하는 문자를 지정
    
    ```html
    <ol type="i">	
    	<li>1</li>
    	<li>2</li>
    </ol>
    <ol type="I">	
    	<li>1</li>
    	<li>2</li>
    </ol>
    <ol type="a">	
    	<li>1</li>
    	<li>2</li>
    </ol>
    <ol type="A">	
    	<li>1</li>
    	<li>2</li>
    </ol>
    <ol type="1">	
    	<li>1</li>
    	<li>2</li>
    </ol>
    ```
    
- `reversed`는 순서를 반대로 시작하도록 지정하는 속성
    - 다른 속성은 `start="4"`와 같이 키(key)와 값(value)을 같이 쓰지만, `reversed`는 키만 사용
    
    ```html
    <ol reversed>  
    	<li>세제</li>
    	<li>돼지 고기 300g</li>
    	<li>생수</li>
    </ol>
    ```
    

### **`<li>` 태그 속성**

- `value = "숫자"`는 해당하는 리스트 아이템의 번호를 지정
    
    ```html
    <ol>	
    	<li value="3">세제</li>
    	<li>돼지 고기 300g</li>
    	<li value="7">생수</li>
    </ol>
    ```
    
    - `value` 속성은 사용하는 항목의 숫자를 기준으로 이후 항목에 숫자가 부여