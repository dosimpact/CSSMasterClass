# CSS Master Class

- section1 flexbox skip
- section2 grid - html 튜토리얼 -> Task하나씩 보면 이해됨
- section3 CSS전처리기 설치
- section4 연습

### 피드백 justify-content | items | self : grid 자체를 움직임 | 그리드 요소가 움직임 | 그리드 요소 안에 가 움직임.

- flex:row에서 justify는 수평 방향, align 은 수직 방향
- flex에서는 justify만 content,items,self가 작동한다..

[https://stackoverflow.com/questions/32551291/in-css-flexbox-why-are-there-no-justify-items-and-justify-self-properties](https://stackoverflow.com/questions/32551291/in-css-flexbox-why-are-there-no-justify-items-and-justify-self-properties)

---

# 1. 그리드 요약 정리

# 그리드 선언을 합니다.

display: grid
gap:

# 그리드 템플릿을 만듭니다.

grid-template-rows: 총 2개의 행을 가지는데, 각 행의 높이를 정한다.
gird-tempalte-columns: 마찬가지..

grid-auto-rows: 다 알아서, 이렇게 적용해,
grid-auto-flow: gird에서 넘치는거는 기본 row으로 연장, 아니 column으로도 가능.

# 그리드 단위를 쫀득하게 지정.

함수: repeat(4,1fr);
단위: 1fr , max-content, min-content,
repeat(auto-fill, minmax(70px,1fr) ); 가능한 많이 채워라, 최소 70px로 만약 애매하게 남는 부분 또는 70px이상의 자리는 1fr로 동등히 나눠서 늘려
repeat(auto-fit, minmax(70px,1fr) ); 가능한 많이 채워라, 최소 70px로 하되, 애매하게 남는부분(70px이하)는 1fr로 늘리고, 70px이상의 자리는 고스트 그리드로 채워라.

# 그리드 자체를 정렬하거나 그리드 안의 개별 요소들을 정렬합니다( 수직 수평 둘다 가능)

justify-content: center 그리드 자체를 row - 수평 중앙정렬
align-content: center 그리드 자체를 column - 수직 중앙정렬

-> place-content 축약 가능

justify-items: center 그리드 요소 안에서 수평 중앙정렬
쌤썜
-> place-itmes 축약 가능

# 그리드 요소의 크기를 지정합니다.( 크기는 1gird-> 2gird 또는 3번에서 5번까지 rule ) flex의 grow 와 유사.

1. 제목 부분은 아예 뺀 위 행을 차지하도록 할 수 있음.
   grid-column: 1 / -1;

---

## 1. flex

- flex -> 기본 row 정렬 -> justify-content (좌우 정렬 ) -> align-items (위 아래 정렬)

[flex guid ](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## 2. Grid

### 그리드 시스템

- flex처럼 하위 요소들 div에게 적용이 된다.

- 그리드 모든 행에대해 어떻게 쪼갤지 행을 나누눈방법을 열 템플릿에 기술
- 그리드의 크기를 반응형으로 만들수있음. minmax 이용
- 그리드 자체를 정렬할수있다. justify-content, align-item
- 그리드 안의 컨테이너들을 정렬할수있음. grid-row-start
- 그리드의 시작점과 끝점을 지정할수있다. | 그리드의 라인을 이름지어서 시작점과 끝점을 설정할수도 있다.

# 3. (이론) PostCSS / CSSNext / CSS4

# 3.0 Installing Parcel (3:54)

- Parcel 멋진 코드를 못생긴 코드로 변환시켜 모든 브라우저가 이해하도록 만들어주는 트렌셀러다.

### 환경 설정

- npm init -y
- npm install parcel-bundler
- npm install postcss-preset-env

- PostCSS는 JS로 CSS를 컴파일 해주는 환경이고 | poestcss-preset-env 가 이제 변화도구중 하나이다.
  [https://postcss.org/](https://postcss.org/)
  [https://preset-env.cssdb.org/](https://preset-env.cssdb.org/)

# 3.1 PostCSS and Parcel (7:13)

- PostCSS 우리의 CSS를 모던하게 바꾸어준다.
- :full-screen 과 같은 가상 선택자를 쓰면, 호환성 문제가 있는데, 자동으로 새로운 코드로 만들어주어 이를 해결!
- css Linter : css에 생길 문제들을 미리 확인해 주는 모듈이다.
- postcss-preset-env : 설치하자 . => css next 였던 프로잭트.

- package.json 셋팅 | stage는 0 1,2,3 이 있는데, 3으로 갈수록 완벽하게 작동하는거, 0으로 갈수록 작동 예정 임!

```js
  "postcss": {
    "plugins": {
      "postcss-preset-env": {
        "stage": 0
      }
    }
  }
```

# 3.2 Functional pseudo-classes (3:05)

# 3.3 CSS Variables (5:14)

# 3.4 @custom-media and Media Query Ranges (5:05)

# 3.5 color-mod, gray(), system-ui (5:42)

# 3.6 Nesting Rules (5:01)

# 3.7 Conclusions (7:30)
