# safari(IOS)에서 outline에 대하여 border-radius가 적용되지 않는 현상

<img src="https://user-images.githubusercontent.com/82315118/220294801-dc5631fe-5369-4267-b95e-5ae4b7667c2c.png" alt="outline사용시 크롬과 사파리 비교" />

> 좌: 크롬 &nbsp;&nbsp;&nbsp;우: 사파리

## 문제 상황

1. 상태에 따라 svg fill이 아닌 png를 바꾸거나 JSX를 변경해야 하는 로직에서 border를 사용하면 리플로우가 발생하면서 레이아웃이 틀어졌었는데 outline으로 레이아웃을 고정시켜두었었다.
2. outline을 사용하니 safari환경에서 border-radius가 적용되지 않는 오류를 발견

outline은 border와 비슷하지만 다르게 동작한다<br>
일단 outline은 해당 엘리먼트와 간섭되지 않고 별개로 외곽선이 만들어진다. 때문에 border와 다르게 엘리먼트 내부 공간에 영향을 미치지 않는다<br>
<br>
때문에 border를 위한 컨테이너를 만들고 `pseudo-class`를 이용해 border 속성으로 해결하거나 `box-shadow`로 해결이 가능하다<br>

<br>

## `box-shadow`적용

<img src="https://user-images.githubusercontent.com/82315118/220296013-a23c60a2-f64d-4b83-aa63-eb0c1da3470c.png" alt="box-shadow적용후 사진" />

> 좌: 크롬 &nbsp;&nbsp;&nbsp;우: 사파리

<br>

**_모바일 환경을 고려해야 하면 outline의 사용을 피해야겟다 :(_**

<br>

적용 소스 코드 <br>

https://github.com/wonjin-dev/gamble/commit/f622cd0a7f154825830c394c8660e72b49cdb91c
