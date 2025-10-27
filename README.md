# Сайт по продаже курсов по выпечке - Wake and Bake

## Описание

ПРОДАЮЩИЙ сайт курсов по выпечке

## Реализация аккордеона

### HTML

```html
<a class="accordion-list__control" href="#">
  <h3 class="accordion-list__control-title">
    Начало кондитерского пути и создание первого торта
  </h3>
  <div class="accordion-list__control-icon">
    <svg
      width="14"
      height="14"
      viewBox="0 0 14 14"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M5.25653 12.96L11.2325 6.984L5.25654 1.008L6.26454 -3.0528e-07L13.2485 6.984L6.26454 13.968L5.25653 12.96Z"
        fill="#FFA55C"
      />
      <path
        d="M12.2402 6.26465L12.2402 7.70465L0.000234839 7.70465L0.000234902 6.26465L12.2402 6.26465Z"
        fill="#FFA55C"
      />
    </svg>
  </div>
</a>
```

### CSS

```css
.accordion-list__item {
  border: 1px solid var(--accent-color);
  border-radius: var(--border-radius);

  margin-bottom: 30px;
}

.accordion-list__item:last-child {
  margin-bottom: 0;
}

.accordion-list__control {
  padding: 41px 30px;
  width: 100%;
  background: transparent;
  text-align: left;

  display: flex;
  justify-content: space-between;
  gap: 15px;

  font-family: "Gabriola";
  font-size: 42px;
  line-height: 90%;
  color: var(--accent-text);
  transition: var(--transition);
}

.accordion-list__item--opened .accordion-list__control {
  padding-bottom: 20px;
}

.accordion-list__control-icon {
  width: 36px;
  height: 36px;
  border: 1.5px solid var(--accent-color);
  border-radius: 50%;
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;

  transition: var(--transition);
}

.accordion-list__control-icon svg {
  margin-left: 2px;
}

.accordion-list__control-icon path {
  transition: var(--transition);
}

.accordion-list__control:hover .accordion-list__control-icon {
  transform: rotate(90deg);
  background: var(--accent-color);
}

.accordion-list__control:hover .accordion-list__control-icon path {
  fill: var(--general-bg);
}

.accordion-list__item--opened .accordion-list__control-icon {
  transform: rotate(90deg);
  background: var(--accent-color);
}

.accordion-list__item--opened .accordion-list__control-icon path {
  fill: var(--general-bg);
}

.accordion-list__content {
  max-height: 0;
  overflow: hidden;
  transition: var(--transition);
}

.accordion-content {
  padding: 0 30px 40px;
  display: flex;
  gap: 80px;
}

.accordion-content__col:first-child {
  max-width: 507px;
  width: 100%;
}

.accordion-content__title {
  text-transform: uppercase;
  line-height: 1.6;
  color: var(--accent-color-2);
  margin-bottom: 20px;
}

.accordion-content__item {
  margin-bottom: 20px;
  display: flex;
}

.accordion-content__item:last-child {
  margin-bottom: 0;
}

.accordion-content__icon {
  width: 24px;
  height: 24px;
  border: 1px solid var(--accent-color-2);
  border-radius: 50%;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin-right: 8px;
  flex-shrink: 0;
}

.accordion-content__text {
  max-width: 274px;
}
```

### JS

```js
<script src="js/fslightbox.js"></script>
```
