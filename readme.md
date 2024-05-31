


# Head, body
1. Head - 브라우저에게 정보를 주는 태그

문서 관련 정보 입력, 웹 브라우저 화면에는 보이지 않음.  
문서에서 사용할 외부 파일 링크
문자 세트 등 문서 정보가 들어있는 <Meta> 태그  
한글로 된 내용을 표시하기 위해서 UTF-8 문자 세트를 사용  
```
meta charset="UTF-8"
```

1. body
실 브라우저에 나타나는 내용


<br/>

# 글자 관련
- ol : ordered list 순서가 있는 **li** 태그 포함가능.  
- ul : unordered list 순서가 없는 리스트

- h1~h9 : 글자크기까지 사용 가능.

- span : 뭔가 묶어줄때 사용.

```
<p> alskntalkntq <span class="redtext">iwtnl</span> knastt</p>
```

<br/>

# 표

- caption : 표 제목
- table : 표 전체
- tr : 행
- td : 셀
- th : 제목 셀 (Head)

<br/>

# 이미지, 오디오, video
```
<img src="" alt=>

<audio src="" controls> </audio>

<video src="" ></video>
```

<br/>

# 하이퍼링크
```
<a href="" target="">
<a> 태그 + href 속성
```

target 없으면 기존창에서 이동, target 있으면 새탭으로 이동.  
각각의 속성은 따로 확인 가능.  
플레이어 표시 없이 배경음악 넣기, 비디오 자동 재생 등등....  
브라우저마다 버전 마다 안되는것도 있으니 참고.  

<br/>

# Form 
- 사용자들에게 정보를 받아들이기 위한 형식

## Label - 뭔가를 구분해줄때 사용.
```
<form action="">
    <label>아이디 : <input type="text"></label>
    <label>비밀번호 : <input type="password"></label>
</form>
```

```
<form action="">
    <label for="user-id">아이디 : </label>
    <input type="text" id="user-id">
    <label>비밀번호 : <input type="password"></label>
</form>
```

위 2개는 같은것. `<label for= > , <input id= >` 는 같아야 같은 묶음으로 인식.
최대, 최소, 기본세팅값 설정가능.
`<input type="number" min="0" max="5" value="2">`  

<br/>

## radio button, checkbox button
- radio : 한개만 선택가능, 한개만 선택하려면 name 속성이 같아야함.  
- checkbox : 여러개 선택가능. **input type에 value를 지정해놔야함. 그래야 value값이 Form에서 넘어감**

그외... 
``` 
<input type="date">
<input type="month">
<input type="week">
<input type="time">
<input type="datetime-local">

hidden 값 사용시
<input type="hidden" name="url" id="url" value="">
```

<br/>

```
required - 반드시 필드에 입력되어야함
<input type="text" id="user-name" required>

readonly - 읽기만 가능
<input type="text" id="addr" value="readonly" readonly>

autofocus - 자동 커서
<input type="text" id="addr" value="readonly" autofocus>
```

## textarea 

```
(영어기준) 가로 40, 세로 4 글자 들어갈 사이즈 입력가능 
<textarea id="memo" cols="40" rows="4"></textarea>
```

## select 
- option 태그로 추가, selected 속성은 기본값.

```
<select>
    <option value="item_1" selected>item1</option>
</select>
```

## datalist 
- option 태그로 항목 추가

```
<datalist id="goods">
    <option value="item_1">item1</option>
</datalist>
```

<br/><br/><br/>

# CSS
내용과 디자인을 구분하기 위해 css html 구분해놓음

스타일 - 각각의 하나하나
스타일시트 - 여러개의 스타일을 한군데 모아놓은것. *.css

html안에 같이 해놓은 내부 스타일시트(보통 `<head>` 내부에 작성) 
                    / 외부 스타일 시트 (파일로 저장)

아래와 같은 형태로 `<link>` 태그, `href` 속성, `rel` 속성의 stylesheet 로 설정.
```
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="css/6.css" rel="stylesheet">
</head>
```


## 선택자

### 전체선택자
```
* {
  ...
}
```

### 특정선택자
```
p {
    ...
}
```
 
### class 선택자
```
.class {
    ...
}
```

### id 선택자 (보통 한번만 쓰기 위한 용도로)
```
#selector {
    ...
}
```

### group 선택자 (여러개 한꺼번에 , 로 구분)
```
h1, p {
    ...
}
```


## 캐스캐이딩 스타일 시트

style이 먼저 적용되는 순서  
!important > 인라인 스타일 > ....


<br/><br/>

# JAVASCRIPT


