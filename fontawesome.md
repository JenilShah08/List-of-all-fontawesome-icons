
Files **FontAwesome-v5.0.9-Pro.json**  and **FontAwesome-v5.0.9-Free.json** above contain a JSON list of FontAwesome 5.0.9 icons.

You may also generate the list of all available icons in order get the latest version:

## Font Awesome Version 5
  1. Go to http://fontawesome.com/cheatsheet/ or https://fontawesome.com/cheatsheet/pro for Pro
  2. Type in console following command
  ```javascript
  [].concat.apply([], Array.prototype.map.call(document.querySelectorAll('.cheatsheet-set'), e => e.id).map(e =>{
    let prefix = '';
    switch (e) {
        case 'regular':
            prefix = 'far'
            break;
        case 'solid':
            prefix = 'fas'
            break;
        case 'light':
            prefix = 'fal'
            break;
        case 'brands':
            prefix = 'fab'
            break;
    }

    return {
        id: e,
        prefix: prefix
    }
}).map(e => Array.prototype.map.call(document.querySelectorAll(`#${e.id} article.icon > dl > .select-all.word-wrap`), element => `${e.prefix} fa-${element.outerText}`))).map(e => `"${e}"`).join(',')
```
  3. Copy

## Font Awesome Version 4
  1. Go to https://fontawesome.com/v4.7.0/icons/
  2. Type in console following command:
  ```javascript
  $(".fontawesome-icon-list i").map(function () { return '"' + this.className + '"'}).toArray().join(',')
  ```
  3. Copy
