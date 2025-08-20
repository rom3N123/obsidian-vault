
## Это WEB API , которое позволяет прикрепить скрытый дом к дом элементу

### ShadowDOM предоставляет инкапсуляцию :
- стили документа не распрастроняются на дом элементы в шадоу доме
- ивенты в шадоу доме не всплывают в дом, но это можно настроить

### Как прикрепить ShadowDOM:
~~~js
const el = document.createElement('div')
const shadowRoot = el.attachShadow({ mode: 'open' })
shadowRoot.innerHTML = "<h1>Я принадлежу Shadow DOM'у</h1>"

~~~

[[Frontend]]