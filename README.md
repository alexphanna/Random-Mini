# Random Mini
### Bookmarklet
```javascript
javascript: (() => {
    let today = new Date();
    let year = 2014 + Math.floor(Math.random() * (today.getFullYear() - 2013));
    let month = Math.floor(Math.random() * 12 + 1);
    if (year == 2014) month = Math.floor(Math.random() * 5 + 8);
    else if (year == today.getFullYear()) month = Math.floor(Math.random() * today.getMonth() + 1);
    let day = Math.floor(Math.random() * new Date(year, month, 0).getDate() + 1);
    if (year == 2014 && month == 8) day = Math.floor(Math.random() * 11 + 21);
    else if (year == today.getFullYear() && month == today.getMonth()) day = Math.floor(Math.random() * today.getDay() + 1);
    window.location.assign("https://www.nytimes.com/crosswords/game/mini/" + year + "/" + month + "/" + day);
  })();
```
