# 네비게이션 만들기

웹 페이지에서 안내판 역할을 하는 네비게이션을 만들어 보겠습니다.
부트스트랩에서는 navbar 라는 클래스를 이용해서 만들며 브라우저(뷰) 사이즈에 따라 네비게이션을 접거나 펼치는 기능을 제공합니다.

http://collectivecollege.net 에서 브라우저를 줄였다가 커졌다 해보면 클 때는 네비게이션 목록에 드러나지만
작아지면 햄버거 표시로 변경되고 해당 아이콘을 클릭하면 밑으로 네비게이션 항목이 나타나는 걸 볼 수 있습니다.

이 전에 작성한 index.html 문서에 이어서 작성합니다.

## navbar 클래스 삽입 

```
<html>
<head>
  <title>Page101</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>
<header>
	<nav class="navbar bg-white">
	  <a class="navbar-brand" href="#">
	  	<button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
	  </a>	 
	</nav>
</header>

<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>

</body>
</html>
```
우선 header와 nav먼저 살펴보겠습니다.

```
<header>
	<nav class="navbar bg-white">
	  <a class="navbar-brand" href="#">
	  	<button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
	  </a>	 
	</nav>
</header>
```

header 태그와 nav 태그를 사용해서 네비게이션 구조를 우선 잡았습니다.

nav 태그에 클래스로 navbar, bg-white 를 주었습니다.
navbar는 네비게이션으로 사용하겠다고 지정하는 역할을 하며 bg-white는 배경이미지 색깔을 흰색으로 지정합니다.

bg-white 와 같은 클래스 이름은 네비게이션 뿐만 아니라 다른 태그에서도 사용가능하며 부트스트랩에서는 primary, secondary, success, danger, warning, info, light, dark, white 색상을 지원합니다.
자세한 사항은 [부트스트랩-컬러](https://getbootstrap.com/docs/4.0/utilities/colors/)에서 확인가능합니다.

## 네비게이션 브랜드 작성

웹페이지를 보면 일반적으로 가장 왼쪽 상단에 웹 페이지의 브랜드나 회사의 로고가 있는 걸 볼 수 있습니다.
네비게이션안에 브랜드를 표시하는 navbar-brand를 삽입합니다.

```
<nav class="navbar bg-white nav-dark">
  <a class="navbar-brand" href="#">
    <button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
  </a>	 
</nav>
```
보통은 회사의 로고 이미지를 사용하는데 collectivecollege에서는 로고가 없기 때문에 ㅠㅠ 버튼 태그를 사용했습니다.
navbar-brand 클래스를 사용하면 부트스트랩에서 패딩 크기, 폰트 크기를 잡아줍니다. 

버튼 태그 안의 클래스 btn, btn-lg, btn-outline-primary 를 사용했고 btn은 버튼으로 표시하게 하고 btn-lg는 버튼의 크기를 lg로 설정하는 것이며 btn-outline-primary는 버튼의 바깥 선의 색을 primary로 지정합니다.

따라서 작성한 html문서를 열어보면 CoCo 의 바깥선이 파란색으로 보이게 됩니다.

## 네비게이션 펼침 기능 만들기

네비게이션이 뷰의 크기에 따라 변하는 기능을 만들어보겠습니다. 크기가 크면 네비게이션 항목이 다 보이고 줄어들면 햄버거 아이콘이 나타나는 기능입니다.

nav 태그에 아래와 같이 변경합니다.

### navbar-expand-lg 삽입

```
<nav class="navbar navbar-dark bg-white navbar-expand-lg">
  <a class="navbar-brand" href="#">
    <button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
  </a>
  
</nav>
```

추가된 클래스는 nav 태그에 navbar-expand-lg 입니다. navbar-expand는 네비게이션 항목을 펼치는 기능을 설정하는 역할을 하며 navbar-expand-lg는 뷰의 크기가 large일 때 펼친다는 뜻입니다. navbar-expand-sm 은 작을 때도 펼치겠다 겠죠?

사이즈를 확인하시려면 [부트스트랩-그리드](https://getbootstrap.com/docs/4.0/layout/grid/)에서 확인할 수 있습니다.

### 토글 버튼 만들기

다음으로 작성할 부분은 브라우저가 작아졌을 때 보여질 토글 버튼입니다.

```
<nav class="navbar navbar-dark bg-white navbar-expand-lg">
  <a class="navbar-brand" href="#">
    <button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
  </a>
  <button class="navbar-toggler bg-primary " type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>	 
  </nav>
```

button 태그에 클래스에 navbar-toggler, br-primary가 적용되었습니다. bg-primary는 배경색을 지정하는 것이며 navbar-toggler는 토클러 역할을 하는 것이라고 부트스트랩에 알려주는 역할을 합니다. 즉 해당 버튼을 클릭하면 네비게이션 항목이 나타난다는 말입니다. data-toggle의 값으로 collapse로 지정하여서 collapse(펼치고 숨기는) 기능을 설정합니다.

data-target는 버튼을 눌렀을 때 나타날 항목들을 포함하는 태그를 설정합니다. #navbarSupportedContent로 설정하였습니다.
그리고 span 태그를 사용하고 class에 navbar-toggle-icon을 사용해서 브라우저가 줄어들 었을 때 햄버거 아이콘이 나타나게 설정합니다.

작성된 문서를 브라우저로 열고 크기를 줄여보면 햄버거 모양이 나타나는 걸 확인할 수 있습니다.

### 네비게이션 항목 만들기

```
<nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-white">
  <a class="navbar-brand" href="#">
    <button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
  </a>
  <button class="navbar-toggler bg-primary " type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="#">홈</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#process">프로세스</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#curriculum">커리큘럼</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#project">프로젝트</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#gallery">갤러리</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#contact">연락하기</a>
      </li>      
    </ul>    
  </div>
</nav>
```

같이 보려면 조금 길어서 collapse 부분만 따로 보겠습니다.

```
<div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
    <ul class="navbar-nav">
      <li class="nav-item">
        <a class="nav-link" href="#">홈</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#process">프로세스</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#curriculum">커리큘럼</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#project">프로젝트</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#gallery">갤러리</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#contact">연락하기</a>
      </li>      
    </ul>    
  </div>
```

클래스로 collapse, navbar-collapse를 삽입하여 copllapse로 지정하며 id로 토클 버튼에서 지정했던 값인 navbarSupportedContent를 설정합니다.

뒤에 오는 ul과 li에는 nav-item, nav-link 클래스를 지정해줍니다.

justify-content-end 클래스는 네비게이션 항목의 위치를 맨 우측에 자리잡게 합니다.

이렇게 하고 브라우저로 해당 문서를 열고 브라우저를 크게하거나 작게 하면 네비게이션 항목이 보이지 않을텐데 잘못 설정된게 아니라 배경색과 텍스트 색이 둘다 하얀색이 보이지 않을 뿐입니다.

style.css 파일을 만들어서 네비게이션 링크 색을 변경하겠습니다.

### style.css 파일 생성

css 폴더를 만들고 안에 style.css 파일을 생성하고 아래와 같이 링크 색을 변경해줍니다.

```
.navbar-dark .navbar-nav .nav-link {
	color: #007bff;
}
```

이제 html문서 head에 style.css를 링크합니다.

```
<head>
  <title>Page101</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
  <link rel="stylesheet" href="css/style.css">
</head>
```

다시 html 문서를 열면 네비게이션 항목이 파란색으로 보이는 것을 확인할 수 있습니다.

햄버거 버튼을 클릭하면 네비게이션 항목들이 보입니다.

현재 까지 만든 html문서는 전제 내용은 아래와 같습니다.

```
<html>
<head>
  <title>Page101</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
<header>
  <nav class="navbar navbar-expand-lg fixed-top ">
	  <a class="navbar-brand" href="#">
	  	<button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
	  </a>
	  <button class="navbar-toggler bg-primary " type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
	    <span class="navbar-toggler-icon"></span>
	  </button>

	  <nav class="navbar navbar-expand-lg fixed-top navbar-dark bg-white">
      <a class="navbar-brand" href="#">
        <button type=button class="btn btn-lg btn-outline-primary">CoCo</button>
      </a>
      <button class="navbar-toggler bg-primary " type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
  
      <div class="collapse navbar-collapse justify-content-end" id="navbarSupportedContent">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" href="#">홈</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#process">프로세스</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#curriculum">커리큘럼</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#project">프로젝트</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#gallery">갤러리</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#contact">연락하기</a>
          </li>
          
        </ul>
        
      </div>
    </nav>
</header>

<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>

</body>
</html>
```




