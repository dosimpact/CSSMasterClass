# CSS Master Class

## 1. flex

- flex -> 기본 row 정렬 -> justify-content (좌우 정렬 ) -> align-items (위 아래 정렬)

[flex guid ](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## 2. Grid

### 그리드 시스템

- flex처럼 하위 요소들 div에게 적용이 된다.

- 그리드 모든 행에대해 어떻게 쪼갤지 행을 나누눈방법을 열 템플릿에 기술
- 그리드의 크기를 반응형으로 만들수있음.
- 그리드 자체를 정렬할수있다.
- 그리드 안의 컨테이너들을 정렬할수있음.
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
