# main 만들기

이 번에는 https://pangol.github.io/page101/ 에서 메인영역을 만들어볼겁니다.
collevtice college 글이 왼편에 있고 설명하는 글이 오른편에 표시되는 형태입니다.

## container, row 만들기

먼저 메인 영역을 div 태그로 만들어줍니다.

```
<div class="container main">
  <div class="row">
		
  </div>
</div>
```

클래스로 container, main을 삽입하고 그 안에 row를 만들어줍니다.
container는 전체 브라우저 크기에서 왼, 오른쪽 패딩을 설정해줍니다. 약간의 여백을 주고 내용을 담을 때 사용합니다.
브라우저의 전체 크기를 사용할 때는 container-fluid 를 사용합니다. row 는 display 속성을 flex로 설정하게 해줍니다. 

## style.css 작업

style.css을 열어서 아래와 같이 패딩 작업을 우선합니다.

```
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
```

## col로 두 개의 영역으로 분리하기

row안을 두 개의 영역으로 분리하겠습니다.

```
<div class="row">
  <div class="col-md-6 text-md-left pr-md-5 order-2">
  </div>
  <div class="col-md-6 text-md-center pr-md-5 order-1 mt-1">
  </div>
</div>
```

영역을 나눌 때 사용하는 클래스는 col-md-6 입니다. 부트스트랩에서는 그리드를 사용해서 영역을 나누는 데 총 12줄의 컬럼(줄)을 사용합니다. 따라서 col-md-6로 설정하면 해당 영역을 6줄을 사용하겠다는 뜻입니다. 각 각 col-md-6 설정해줬습니다. md는 브라우저 크기를 설정해준 것입니다. md 크기 이상이면 6줄을 사용한다는 말입니다. 브라우저가 md보다 작을 때는 12칸을 모두 차지하게 됩니다.

text-md-left 는 텍스트의 위치를 왼쪽으로 설정하는 것이고 pr-md-5는 padding right 값을 5로 설정하는 것입니다. 5는 픽셀값이 아니라 실제로는 3rem으로 설정됩니다. 

order-2는 브라우저 크기가 작아질 때 두 개의 영역모두 12칸을 차지하게 되는 데 이 때 우선적으로 표시될 순서를 알려주는 것입니다. 즉 브라우저 크기가 작을 때는 order-1을 가진 영역이 우선 표시됩니다.

mt-1 은 margin-top을 말합니다.

두 개의 영역에 콘텐츠를 삽입합니다.

```
<div class="container main">
  <div class="row">
    <div class="col-md-6 text-md-left pr-md-5 order-2">
      <p class="lead">
        같이 만들고, 같이 배우며, 같이 개선합니다<br>
        배워서 우리에게 줍니다.
      </p>
      <p class="lead mb-4">
        <strong>정보의 불균형</strong><strong>교육의 불평등</strong>을 해결하기 위해
        <br>
        Collective College는 협력을 통해 지식을 만들고 참여를 통해 개선하고 결과물을 나눕니다. 
        소수에게 지식이 편중되는 문제를 해결하려고 합니다.
        <br><br>
        <strong>협업을 통해 지식과정을 만들고 공유합니다.</strong> 
      </p>
    </div>
    <div class="col-md-6 text-md-center pr-md-5 order-1 mt-1">
      <h1 class="text-primary ">Collective College</h1>
      <br>
    </div>
  </div>
</div>
```

lead는 font-size, font-weight에 변화를 주는 클래스며 text-primary는 텍스트의 색을 변경합니다.


## style.css 문서

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
```
