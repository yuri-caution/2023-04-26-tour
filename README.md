#  tour 웹사이트

### header 고정, vh 사용
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


### header 요소 배치 (flex, gap 말고)
.header {
    height: 80px;
    display: flex;
    align-items: center;
    padding: 0 30px;
}

.logo {
    margin-right: auto;
}


### :hover 에 라인 넣기 ::after 사용
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

### hover 에 라인 넣기 border 사용

.gnb li a:hover {
    color: #3ec9cb;
    border-bottom: 3px solid #3ec9cb;
}

/* .on 붙여서 써야함 */
.gnb li.on a {
    color: #3ec9cb;
    border-bottom: 3px solid #3ec9cb;
}