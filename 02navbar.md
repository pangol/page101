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
<nav class="navbar bg-white">
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


