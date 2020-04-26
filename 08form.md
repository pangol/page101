# 연락하기 영역 만들기

https://99college.org/ 에서 연락하기 영역을 만들어보겠습니다.
form 을 꾸미는 방법에 대해서 알아봅니다.

## 틀 잡기, justify-content-center

```
<div class="contact" id="contact">
  <div class="row justify-content-center">
    <div class="col-md-6 col-sm-12">
    </div>
  </div>
</div>
```

연락하기는 크기 전체를 사용하기 때문에 container를 설정하지 않았습니다.
row 가 있는 요소에 justify-content-center를 사용해서 그 안에 작성된 컨텐츠를 중앙에 위치하게 설정했습니다.
전체 크기를 다 사용하지만 컨텐츠의 크기는 절반만큼만 사용하기 위해서 col-md-6를 설정했습니다.

## form 작성하기

### form-gorup

```
<div class="contact" id="contact">
  <div class="row justify-content-center">
    <div class="col-md-6 col-sm-12">
      <form>
        <div class="form-group row">
          <label for="inputEmail" class="col-sm-2 col-form-label">이메일</label>
          <div class="col-sm-10">
            <input type="email" class="form-control" id="inputEmail" placeholder="Email">
          </div>
        </div>
      </form>
    </div>
  </div>
</div>
```

form 태그 안에 입력받을 정보를 form-froup를 사용해서 하나의 그룹으로 표현합니다. row는 label과 input이 행으로 표시되게 하는 역할입니다. label에는 클래스 col-form-label을 작성해줍니다. input class에는 form-control을 입력합니다.

총 세 개의 인풋을 받기 때문에 세 번 반복합니다.

```
<form>
  <div class="form-group row">
    <label for="inputEmail" class="col-sm-2 col-form-label">이메일</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="inputEmail" placeholder="Email">
    </div>
  </div>
  <div class="form-group row">
    <label for="contactName" class="col-sm-2 col-form-label">이름</label>
    <div class="col-sm-10">
      <input type="text" class="form-control" id="contactName" placeholder="Enter Name">
    </div>
  </div>
  <div class="form-group">
    <textarea class="form-control" id="contactTextarea" rows="5" placeholder="문의 사항을 적어주세요"></textarea>
    <small>이 폼은 예시를 위해 만들어서 동작하지 않습니다.</small>
  </div>
</form>
```

### button 작성하기

```
<form>
  <div class="form-group row">
    <label for="inputEmail" class="col-sm-2 col-form-label">이메일</label>
    <div class="col-sm-10">
      <input type="email" class="form-control" id="inputEmail" placeholder="Email">
    </div>
  </div>
  <div class="form-group row">
    <label for="contactName" class="col-sm-2 col-form-label">이름</label>
    <div class="col-sm-10">
      <input type="text" class="form-control" id="contactName" placeholder="Enter Name">
    </div>
  </div>
  <div class="form-group">
    <textarea class="form-control" id="contactTextarea" rows="5" placeholder="문의 사항을 적어주세요"></textarea>
    <small>이 폼은 예시를 위해 만들어서 동작하지 않습니다.</small>
  </div>
	<button type="submit" class="btn btn-primary float-right">전송하기</button>
</form>
```
버튼으로 표시하기 위해서 클래스에 btn, 색을 지정하는 btn-primary를 사용했습니다.
버튼을 우측으로 위치 시키기 위해서 float-right을 설정했습니다.

