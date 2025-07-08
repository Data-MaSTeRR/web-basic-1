# To make a "Travel Info Page" 

- https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Structuring_documents
- header-main-footer의 html 구조
- https://academind.com/tutorials/css-grid-vs-flexbox/
- CSS의 FLEX와 GRID를 잘쓰도록 훈련

## 📐 CSS Flexbox vs Grid 차이 정리

---

## ✨ 핵심 개념

| 특징        | **Flexbox**                    | **Grid**                  |
| --------- | ------------------------------ | ------------------------- |
| 레이아웃 차원   | **1차원 (row 또는 column)**        | **2차원 (row + column)**    |
| 주 용도      | 아이템 간 정렬, 공간 분배                | 전체 레이아웃 구성, 영역 설계         |
| 배치 기준     | 주축(main axis)와 교차축(cross axis) | 행(row)과 열(column)을 동시에 지정 |
| 유연성       | 콘텐츠 크기에 따라 유동적                 | 고정된 레이아웃, 정교한 제어 가능       |
| 코드 작성 난이도 | 간단, 직관적                        | 약간 복잡하지만 구조화에 유리          |

---

## 🧰 Flexbox (Flexible Box)

* 한 방향(가로 또는 세로)으로 아이템을 정렬하는 데 유용
* 주로 작은 UI 요소(버튼 그룹, 메뉴, 카드 등)에 적합
* `justify-content`, `align-items`로 정렬 제어
* `flex-grow`, `flex-shrink`, `flex-basis`로 아이템 크기 조절

```css
.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
```

---

## 🧱 Grid

* 행과 열을 동시에 정의해 복잡한 레이아웃을 설계
* 페이지 전체나 대형 섹션의 구조화에 적합
* `grid-template-rows`, `grid-template-columns`로 레이아웃 설계
* 격자 형태의 정렬에 강력

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto;
  gap: 10px;
}
```

---

## 🔷 언제 사용하면 좋을까?

| 상황                  | 추천 도구       |
| ------------------- | ----------- |
| 한 방향 정렬, 유연한 콘텐츠 배치 | **Flexbox** |
| 2차원 구조, 페이지 레이아웃    | **Grid**    |
| 작은 컴포넌트 정렬          | **Flexbox** |
| 전체 레이아웃 설계          | **Grid**    |

---

## 📝 요약

> ✅ **Flexbox**: 1차원 레이아웃, 콘텐츠 중심, 간단한 정렬에 적합
> ✅ **Grid**: 2차원 레이아웃, 레이아웃 중심, 복잡한 구조 설계에 적합

---

📌 실무에서는 두 가지를 **혼합해서 사용**하는 경우가 많습니다.
예) Grid로 큰 틀을 만들고, 내부 요소는 Flexbox로 정렬
