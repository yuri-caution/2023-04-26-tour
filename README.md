#  tour 웹사이트

### header 고정, vh 사용
```
.wrap {
    background-color: red;
}

.header {
    background-color: aqua;
    height: 90px;
}

.hero {
    background-color: yellow;
    height: calc(100vh - 90px);
}
```

### header 요소 배치 (flex, gap 말고)
```
.header {
    height: 80px;
    display: flex;
    align-items: center;
    padding: 0 30px;
}

.logo {
    margin-right: auto;
}
```


### :hover 에 라인 넣기 방법1 ::after 사용
```
.gnb li a {
    padding: 30px 0;
    position: relative;
}

.gnb li a:hover {
    color: #3ec9cb;
}

.gnb li a:hover:after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    height: 3px;
    width: 100%;
    background-color: #3ec9cb;
}

/* .on 붙여서 써야함 */
.gnb li.on {
    color: #3ec9cb;
}

.gnb li.on a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    height: 3px;
    width: 100%;
    background-color: #3ec9cb;
}
```

### hover 에 라인 넣기 방법2 border 사용
```
.gnb li a:hover {
    color: #3ec9cb;
    border-bottom: 3px solid #3ec9cb;
}

/* .on 붙여서 써야함 */
.gnb li.on a {
    color: #3ec9cb;
    border-bottom: 3px solid #3ec9cb;
}


### 글자 중앙 고정 배치 (position, 사용)
.hero {
    height: calc(100vh - 80px);
    background-image: url("../img/hero.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: 200%;
    position: relative;
}

.hero .text_box {
    position: absolute;
    top: 50%;
    left: 50%; 
    transform: translate(-50%, -50%);
    color: #fff;
    text-align: center;
}
```


### 아이콘 배치 (position 사용)
```
.social {
    position: absolute;
    top: 50%;
    right: 30px;
    transform: translateY(-50%);
    display: flex;
    flex-direction: column;
    gap: 40px;
}

/* position: absolute; 하면 넓이 사라짐. */
/* 다시 넓이 잡아줄 것 */
.hero .bottom {
    display: flex;
    justify-content: space-between;
    padding: 0 30px;
    position: absolute;
    bottom: 30px;
    left: 0;
    width: 100%;
}
```

### 아이콘 컬러 번경 (외부 코드 참고)
```
.hero img {
    width: 30px;
    filter: brightness(0) invert(1);
}
```

### 백그라운드 이미지에 그라디언트 적용
##### bg 마크업 추가 (text_box보다 위에)
##### css 그라디언트 코드 (css gradient generator)
```
.hero {
    height: calc(100vh - 80px);
    background-image: url("../img/hero.jpg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: 200%;
    position: relative;
}

.hero .bg {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(0deg, rgba(0,0,0,1) 0%, rgba(0,0,0,0) 70%);
}

.hero .text_box {
    position: absolute;
    top: 50%;
    left: 50%; 
    transform: translate(-50%, -50%);
    color: #fff;
    text-align: center;
}
```