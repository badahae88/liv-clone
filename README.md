
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
## 느낀점
- 정말.. 오래 걸린다.... 시간과 공간의 방이다..
## 진행경과
### '23.06.29
![0629-liv-clone](https://github.com/badahae88/liv-clone/assets/137893145/66012a60-010a-484a-8d81-b622a76b44a2)

