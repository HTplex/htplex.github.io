How to remove annoying header on Github Pages:

create file on root folder: `/assets/css/style.scss`
with the following code inside:
```scss
---
---

@import "{{ site.theme }}";

header {
  display: none;
}
```