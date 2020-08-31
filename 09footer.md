# 푸터 만들기

https://pangol.github.io/page101/ 에서 푸터 영역을 만듭니다.

## 바로 작성하기

```
<footer class="bd-footer text-muted">
  <div class="container-fluid p-3 p-md-5">
    <p>Made by Colletive College
      <a href="https://www.facebook.com/99colleage/" target="_blank">
        <i class="fab fa-facebook-square fa-lg"></i>
      </a>
    </p>
    <address>
      Written by <a href="mailto:pangol75@gmail..com">KENTA</a>
      <a href="https://github.com/pangol" target="_blank">
        <i class="fab fa-github fa-lg"></i>
      </a>
    </address>
  </div>
</footer>
```
부트스트랩에 bd-footer 는 없습니다. 푸터의 배경색을 지정하기 위해서 임의로 만들었습니다.
text-muted는 글씨 색을 회색으로 지정합니다.

## style.css 작성

```
.bd-footer{
	background-color: #f7f7f7;
}
```

이렇게 부트스트랩으로 만드는 원페이지 101이 마무리 되었습니다.
학습하시면서 오타를 발견하셨거나 건의사항이 있으시면 언제든지 플리퀘 환영합니다.
공부하느라 수고하셨습니다.