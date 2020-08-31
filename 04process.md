# process 영역 만들기

https://99college.org/ 에서 process 영역을 만들어보겠습니다
이 번에는 container-fluid, card-column 을 사용해서 영역을 나눕니다.

## 틀 잡기, card-columns

process 콘텐츠를 작성할 틀을 생성합니다.

```
<div class="process container-fluid bg-primary text-white" id="process">
  <div class="container ">
    <div class="row">
    <div class="card-columns">
      
    </div>
    </div>
  </div>
</div>
```

container-fluid를 사용해서 브라우저 전체 크기를 사용했고 bg-primary로 배경색 지정, text-white로 글씨색을 지정했습니다.
container-fluid안에 container 클래스를 사용해서 안에 내용들은 전체 브라우저를 사용하지 않게 했습니다.
그 안에 row를 사용해서 display를 flex로 설정해줬습니다.

이 번에는 col을 사용하지 않고 card-columns를 사용했습니다. card-columns는 자동으로 컬럼의 수를 3으로 설정해줍니다.

## card 를 사용해서 컬럼 채우기

```
<div class="card-columns">
  <div class="card bg-primary border-primary">
    <div class="card-body">
      <h5 class="card-title"><i class="fas fa-marker"></i> 공유지 </h5>
      <p class="card-text"> 스터디, 강의, 제품 만들고 싶은 주제를 선정하고 최소한의 공유지를 만듭니다</p>
    </div>
  </div>
  <div class="card bg-primary border-primary">
    <div class="card-body">
      <h5 class="card-title"><i class="fas fa-hands-helping"></i> 참여, 협업을 통한 개선</h5>
      <p class="card-text">누구나 참여 가능한 플랫폼, 협업 도구를 적극적으로 사용합니다. 프로토타입을 개선합니다.</p>
    </div>
  </div>
  <div class="card bg-primary border-primary ">
    <div class="card-body">
      <h5 class="card-title"><i class="fab fa-slideshare"></i> 공유</h5>
      <p class="card-text">만들어진 제품의 소스와 과정 또한 공개합니다.<br>
        오픈소스, 오픈하드웨어, 오픈프로세스를 지향합니다.
        공유와 협업을 통해 정보의 불평등을 해결할 수 있습니다.</p>
    </div>
  </div>
</div>
```

카드 모양을 만들 때는 card 태그를 만들고 그 안에 card-header, card-body, card-footer로 구성됩니다.
이 번에는 card-body만 사용해서 만들었습니다. card-body안에 card-title, card-text를 사용해서 작성합니다.
border-primary 는 보더의 색을 설정하는 것입니다.

## 아이콘 삽입하기

프로세스 영역안에 <i class="fas fa-marker"> 이 부분은 아이콘을 만들어주는 부분입니다.
font awesome 이라는 라이브러리를 사용했습니다. 아이콘을 폰트처럼 사용할 수 있게 만들어줍니다.
자세한 설명은 https://fontawesome.com/ 에 나와있습니다.

fontawesome을 사용하기 위해서는 부트스트랩 처럼 html문서에 링크를 걸어줍니다. 
head 부분을 아래와 같이 변경합니다.

```
<head>
  <title>Page101</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
  <link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.4.1/css/all.css" integrity="sha384-5sAR7xN1Nv6T6+dT2mhtzEpVJvfS3NScPQTrOxhwjIuvcA67KV2R5Jz6kr4abQsz" crossorigin="anonymous">
  <link rel="stylesheet" href="css/style.css">
</head>
```

# style.css 변경하기

영역끼리의 사이를 설정합니다.
style.css를 열어서 아래와 같이 변경합니다.

```
.navbar-dark .navbar-nav .nav-link {
	color: #007bff;
}

.navbar-dark .navbar-nav .nav-link:hover {
	color: black;
}

.main{
	padding: 8rem 15px;
	padding-bottom: 3rem;
	
}


.main h1 {
	font-size: 3.5rem;
	font-weight: bold;
}

.main strong{
	font-weight: bold;
}

.process, .curriculum, .project, .gallery, .contact{
	padding: 3rem 15px;
}

.process {
	margin-bottom: 3rem;
}

```
