# 부트스트랩 소개
부트스트랩은 트위터에서 만든 프런트 엔드 컴포넌트 라이브러리입니다. 부트스트랩을 사용하면 빠르고 쉽게 웹 페이지를 꾸밀 수 있습니다. 

자세한 설명은 [부트스트랩 웹페이지](https://getbootstrap.com/)에서 확인하실 수 있습니다.

# 부트스트랩 설정하기
html문서에서 부트스트랩을 사용하기 위해서는 부트스트랩 라이브러리를 직접 다운로드 하는 방법과 CDN을 사용하는 방법 두 가지가 있습니다. 

여기에서는 직접 다운로드 하지 않고 CDN을 이용하겠습니다.

## index.html 문서 만들기
프로젝트를 진행할 폴더를 생성합니다.
해당 폴더로 이동한 후에 index.html 문서를 생성합니다.

index.html문서를 열어 아래와 같이 작성합니다.

```
<html>
<head>
  <title>Page101</title>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/css/bootstrap.min.css" integrity="sha384-MCw98/SFnGE8fJT3GXwEOngsV7Zt27NXFoaoApmYm81iuXoPkFOJwJ8ERdknLPMO" crossorigin="anonymous">
</head>
<body>


<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.3/umd/popper.min.js" integrity="sha384-ZMP7rVo3mIykV+2+9J3UJ46jBk0WLaUAdn689aCwoqbBJiSnjAK/l8WvCWPIPm49" crossorigin="anonymous"></script>
<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.1.3/js/bootstrap.min.js" integrity="sha384-ChfqqxuZUCnJSK3+MXmPNIyE6ZbWh2IMqE241rYiqJxyMiZ6OW/JmZQ5stwEULTy" crossorigin="anonymous"></script>

</body>
</html>
```

부트스트랩을 사용하기 위해서는 css, js 파일 뿐만 아니라 proper, jquery파일을 링크해야 합니다.
html 문서의 head안에 bootstrap.min.css, body 안에 jquery-3.3.1, popper.js, bootstrap.min.js를 삽입합니다.

위의 파일들의 CDN 주소를 확인하려면 [부트스트랩 웹페이지](https://getbootstrap.com/)에서 가능합니다.

부트스트랩 버전이 바뀌면 해당 CDN의 주소도 변경되니 CDN링크를 사용할 때는 웹 페이지에서 먼저 확인하시기 바랍니다.
