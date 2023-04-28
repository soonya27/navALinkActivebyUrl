# navALinkActivebyUrl

## 현재 url과 navbar a의 href을 비교하여 해당 nav active class 추가 스크립트

### code
```javascript

//vallila JS
const navBarA = document.querySelectorAll('#footerNav li a');
const array = Array.from(navBarA).filter(function (item) {
    const currUrl = document.location.href;
    const navUrl = item.getAttribute('href');
    return currUrl.includes(navUrl);
});
array.forEach(function (item) {
    item.parentElement.classList.add('active');
});

//jquery
// $('#footerNav li a').filter(function () {
//     const currUrl = document.location.href;
//     const navUrl = $(this).attr('href').split('/')[2];
//     return currUrl.includes(navUrl);
// }).closest('li').addClass('active');

```
