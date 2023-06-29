# 내가 좋아하는 리브 자전거
## 새로 알게 된 점
- 쌍따옴표 안에는 작은 따옴표만 된다
  ```javascript
  <button @click="$emit('closeModal','')">닫기</button>
  ```
- 영역안에 세 요소를 왼쪽끝, 중앙, 오른쪽 끝으로 가로 정렬 하기
  ```css
  .1st-child{
    margin-right: auto;
  }
  .3rd-child{
    margin-left: auto;
  }
  ```
- 인풋은 기본적으로 문자열이므로 숫자로 바꿔주려면 `v-model.number`이용
  ```javascript
  <input v-model.number="month" type="range" min="1" max="12">
  ```
## 보완할 점
- 정렬 버튼 못만들었다. 위에 위치를 고정한 메뉴바 때문에 가리는데 어떻게 해야할 지 모르겠다.
- 모달창이 모달 컴포넌트를 App.vue에서 메뉴컴포넌트보다 먼저 위치시켰는데도 메뉴에 가린다. 어떻게 해결해야 하지?
## 진행경과
### '23.06.29
![0629-liv-clone](https://github.com/badahae88/liv-clone/assets/137893145/66012a60-010a-484a-8d81-b622a76b44a2)

![0629-liv-clone(2)](https://github.com/badahae88/liv-clone/assets/137893145/fbe27816-6267-4fe2-8848-3ff3b69a5e4c)
