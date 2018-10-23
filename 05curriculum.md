# curriculum 영역 만들기

http://collectivecollege.net 에서 curriculum 영역을 만들어보겠습니다
이 번에는 card-deck 을 사용해서 영역을 나누는 방법과 modal을 사용하는 방법에 대해서 배웁니다.
modal은 버튼 클릭 시 팝업창이 나타나는 기능을 말합니다.

## 틀 잡기, card-deck

container를 만들고 그 안에 card-deck 만듭니다.
card-deck은 카드 들 간에 동일한 크기(가로, 세로)로 컬럼을 생성하려고 할 때 사용합니다.

```
<div class="curriculum container" id="curriculum">
	<div class="card-deck">
	  <div class="card border border-primary mb-3 ">
	  </div>
	  <div class="card border border-primary mb-3 ">
	  </div>
	  <div class="card border border-primary mb-3 ">
	  </div>
	</div>
</div>

```
card-deck안에 만들려고 하는 card를 생성합니다.
border, border-primary는 색 관련 설정이며 mb-3은 margin-bottom 설정입니다.

## card안 꾸미기

card-body를 만들고 안에 card-title, card-text를 만들어 줍니다.

```
<div class="card border border-primary mb-3 ">
  <div class="card-body">
    <h5 class="card-title">Web</h5>
    <p class="card-text">웹을 만들 때 필요한 지식을 배웁니다. <br>
      프런트엔드, 백엔드, 인프라를 다루는 과정입니다. </p>
    <p class="card-text d-flex justify-content-end">
      <button type="button" class="btn btn-outline-primary btn-xs" data-toggle="modal" data-target="#readMore1">더 보기</button>
    </p>
  </div>
</div>
```
커리큘럼의 경우 '더 보기'를 클릭하면 관련 내용이 팝업처럼 나오게 설정되어 있기 때문에 card-text 안에 button을 생성해주었습니다.

d-flex는 display를 flex로 설정하는 것이며 justify-content-end는 위치를 오른쪽으로 설정하는 방법입니다.

팝업 창처럼 나타나게 하기 위해서는 data-toggle의 값을 modal로 설정해야 합니다. 그리고 팝업의 내용을 data-target의 값으로 지정하면 됩니다.

## Modal 만들기

팝업창에 나타날 부분을 작성해보겠습니다.

```
<div class="card-body">
  <h5 class="card-title">Web</h5>
  <p class="card-text">웹을 만들 때 필요한 지식을 배웁니다. <br>
    프런트엔드, 백엔드, 인프라를 다루는 과정입니다. </p>
  <p class="card-text d-flex justify-content-end">
    <button type="button" class="btn btn-outline-primary btn-xs" data-toggle="modal" data-target="#readMore1">더 보기</button>
  </p>
  <!-- Modal -->
  <div class="modal fade" id="readMore1" tabindex="-1" role="dialog" aria-labelledby="readMore1" aria-hidden="true">
    <div class="modal-dialog" role="document">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel">웹</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
        <div class="modal-body">
          <h6>인프라</h6>
          <p>서버를 구성하는 방법에 대한 공부를 합니다.</p>
          <p>라즈베리 파이를 통한 실제 서버 구축</p>
          <p>아마존, 애저 등 클라우드 서비스를 이용한 구축</p>
          <br>
          <hr>
          <h6>프런트엔드</h6>
          <p>html문서를 만드는 데 필요한 것을 공부합니다.</p>
          <p>html, css, javascript, jQeury</p>
          <p>Framwork - bootstrap 등</p>
          <br>
          <hr>
          <h6>백엔드</h6>
          <p>웹서버를 구성하는 어플리케이션에 대해서 공부합니다.</p>
          <p>Web Framework, Database, MVC model</p>
          <p>NODE.jS EXPRESS DJANGO MySQL MONGODB 등</p>
        </div>
        <div class="modal-footer">
          <button type="button" class="btn btn-primary" data-dismiss="modal">닫기</button>
        </div>
      </div>
    </div>
  </div>
</div>
```

전체를 보려면 복잡하니 Modal 부분만 따로 보겠습니다.


```
<div class="modal fade" id="readMore1" tabindex="-1" role="dialog" aria-labelledby="readMore1" aria-hidden="true">
  <div class="modal-dialog" role="document">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="exampleModalLabel">웹</h5>
        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
          <span aria-hidden="true">&times;</span>
        </button>
      </div>
      <div class="modal-body">
        <h6>인프라</h6>
        <p>서버를 구성하는 방법에 대한 공부를 합니다.</p>
        <p>라즈베리 파이를 통한 실제 서버 구축</p>
        <p>아마존, 애저 등 클라우드 서비스를 이용한 구축</p>
        <br>
        <hr>
        <h6>프런트엔드</h6>
        <p>html문서를 만드는 데 필요한 것을 공부합니다.</p>
        <p>html, css, javascript, jQeury</p>
        <p>Framwork - bootstrap 등</p>
        <br>
        <hr>
        <h6>백엔드</h6>
        <p>웹서버를 구성하는 어플리케이션에 대해서 공부합니다.</p>
        <p>Web Framework, Database, MVC model</p>
        <p>NODE.jS EXPRESS DJANGO MySQL MONGODB 등</p>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn btn-primary" data-dismiss="modal">닫기</button>
      </div>
    </div>
  </div>
</div>
```
태그에 modal를 삽입하고 팝업으로 나타날 때 효과인 fade를 적습니다. 그리고 id로 위의 버튼 태그에서 설정한 data-target값을 사용합니다. role은 dialog로 설정합니다.

그 안에 modal-dialog와 role로 document를 설정합니다. 후에 modal-content를 만듭니다.
modal-content는 modal-header, modal-body, modal-footer 로 구성됩니다.

modal-header에는 modal-title로 modal의 제목을 modal-body에는 본문의 내용을 작성합니다.
modal-footer에는 닫기 버튼을 만들어줍니다.

닫기 버튼이 정상동작을 하기 위해서는 data-dimiss="modal"이 설정되어 있어야 합니다.

이 걸 세 번 반복합니다. ^^;;

## 전체 curriculum 영역

```
<div class="curriculum container" id="curriculum">
	<div class="card-deck">
	  <div class="card border border-primary mb-3 ">
	    <div class="card-body">
	      <h5 class="card-title">Web</h5>
				<p class="card-text">웹을 만들 때 필요한 지식을 배웁니다. <br>
					프런트엔드, 백엔드, 인프라를 다루는 과정입니다. </p>
	      <p class="card-text d-flex justify-content-end">
	      	<button type="button" class="btn btn-outline-primary btn-xs" data-toggle="modal" data-target="#readMore1">더 보기</button>
	      </p>
	      <!-- Modal -->
				<div class="modal fade" id="readMore1" tabindex="-1" role="dialog" aria-labelledby="readMore1" aria-hidden="true">
				  <div class="modal-dialog" role="document">
				    <div class="modal-content">
				      <div class="modal-header">
				        <h5 class="modal-title" id="exampleModalLabel">웹</h5>
				        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
				          <span aria-hidden="true">&times;</span>
				        </button>
				      </div>
				      <div class="modal-body">
								<h6>인프라</h6>
								<p>서버를 구성하는 방법에 대한 공부를 합니다.</p>
								<p>라즈베리 파이를 통한 실제 서버 구축</p>
								<p>아마존, 애저 등 클라우드 서비스를 이용한 구축</p>
								<br>
								<hr>
								<h6>프런트엔드</h6>
								<p>html문서를 만드는 데 필요한 것을 공부합니다.</p>
								<p>html, css, javascript, jQeury</p>
								<p>Framwork - bootstrap 등</p>
								<br>
								<hr>
								<h6>백엔드</h6>
								<p>웹서버를 구성하는 어플리케이션에 대해서 공부합니다.</p>
								<p>Web Framework, Database, MVC model</p>
								<p>NODE.jS EXPRESS DJANGO MySQL MONGODB 등</p>
				      </div>
				      <div class="modal-footer">
				        <button type="button" class="btn btn-primary" data-dismiss="modal">닫기</button>
				      </div>
				    </div>
				  </div>
				</div>
	    </div>
	  </div>
	  <div class="card border border-primary mb-3 ">
	    <div class="card-body">
	      <h5 class="card-title">BlockChain</h5>
	      <p class="card-text">블록체인 개념, 아키텍쳐 설계, Dapp만들기를 배우는 과정입니다.</p>
	      <p class="card-text d-flex justify-content-end">
	      	<button type="button" class="btn btn-outline-primary btn-xs" data-toggle="modal" data-target="#readMore2">더 보기</button>
	      </p>
	      <!-- Modal -->
				<div class="modal fade" id="readMore2" tabindex="-1" role="dialog" aria-labelledby="readMore2" aria-hidden="true">
				  <div class="modal-dialog" role="document">
				    <div class="modal-content">
				      <div class="modal-header">
				        <h5 class="modal-title" id="readMore2">블록체인</h5>
				        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
				          <span aria-hidden="true">&times;</span>
				        </button>
				      </div>
				      <div class="modal-body">
									<h6>블록체인 기초</h6>
									<p>블록체인을 구성하는 기본 개념에 대해 공부합니다.</p>
									<p>기초 기술에 대해 python등을 통해 구현</p>
									<br>
									<hr>
									<h6>아키텍쳐 설계</h6>
									<p>블록체인 엔진에 대한 평가기준 작성과 분석을 하는 과정</p>
									<p>비트코인, 이더리움, 텐더민트 등 다양한 블록체인 엔진을 분석합니다.</p>
									<p>분석을 토대로 설계를 합니다.</p>
									<br>
									<hr>
									<h6>Dapp</h6>
									<p>블록체인 위에 실행되는 어플리케이션을 만드는 과정입니다.</p>
									<p>이더리움, 이오스 등 다양한 엔진 위에서 실행되는 Dapp을 만들어봅니다.</p>
									<p>Dapp과 관련된 보안요소도 살펴봅니다.</p>
									<a href="https://github.com/pangol/dapp101">Dapp101보러 가기</a>
				      </div>
				      <div class="modal-footer">
				        <button type="button" class="btn btn-primary" data-dismiss="modal">닫기</button>
				      </div>
				    </div>
				  </div>
				</div>
	    </div>
	  </div>
	  <div class="card border border-primary mb-3 ">
	    <div class="card-body">
	      <h5 class="card-title">인공지능과 데이터 분석</h5>
	      <p class="card-text">데이터 분석과 인공지능에 필요한 지식을 배우는 과정입니다.</p>
	      <p class="card-text d-flex justify-content-end">
	      	<button type="button" class="btn btn-outline-primary btn-xs" data-toggle="modal" data-target="#readMore3">더 보기</button>
	      </p>
	      <!-- Modal -->
				<div class="modal fade" id="readMore3" tabindex="-1" role="dialog" aria-labelledby="readMore3" aria-hidden="true">
				  <div class="modal-dialog" role="document">
				    <div class="modal-content">
				      <div class="modal-header">
				        <h5 class="modal-title" id="readMore3">인공지능과 데이터 분석</h5>
				        <button type="button" class="close" data-dismiss="modal" aria-label="Close">
				          <span aria-hidden="true">&times;</span>
				        </button>
				      </div>
				      <div class="modal-body">
									<h6>파이썬 기초</h6>
									<p>데이터 분석과 인공지능에 많이 사용되는 파이썬 기초를 공부합니다.</p>
									<p>가장 기본적인 데이터분석과 인공지능 기술에 대해 배웁니다.</p>
									<br>
									<hr>
									<h6>인공지능</h6>
									<p>신경망을 다루는 방법에 대해 학습합니다.</p>
									<p>이미지 분석, 자연어 처리 등에 필요한 부가적인 정보도 학습니다.</p>
									<br>
									<hr>
									<h6>데이터 분석</h6>
									<p>데이터 분석의 기초인 확률</p>
									<p>SQL 다루기</p>									
				      </div>
				      <div class="modal-footer">
				        <button type="button" class="btn btn-primary" data-dismiss="modal">닫기</button>
				      </div>
				    </div>
				  </div>
				</div>
	    </div>
  	</div>
	</div>
</div>
```

# style.css 변경하기

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

.curriculum h5{
	font-weight: bold; 
}

.modal-title {
	font-weight: bold;
}

.modal-body h6 {
	font-weight: bold;
}

.card-title {
	font-weight: bold;
}

```
