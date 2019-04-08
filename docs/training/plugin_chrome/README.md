# Treinamento de Git

**Resposáveis**: [Cleber Castro](https://github.com/cjjcastro)

**Data**: 03/04/2019

**Membros do Time que Compareceram**: [Francisco](https://github.com/FranciscoHeronildo), [Vitor Alves](https://github.com/vitorAlves7), [Vitor Meireles](https://github.com/VitorMeirelesOliveira)

## Formato do Treinamento

Foi desenvolvido e apresentado um plugin de chrome para a equipe de MDS.

## Código desenvolvido no treinamento

### manifest.json

```json
{
    "name":"chrome-extension",
    "manifest_version":2,
    "description": "my chrome extension",
    "version":"1.0",
    "permissions": [
        "tabs",
        "unlimited_storage",
        "notifications",
        "contextMenus",
        "cookies",
        "storage",
        "idle",
        "activeTab"
    ],
    "browser_action":{
        "default_popup": "popup.html"
    },
    "content_scripts": [
        {
            "matches": [
                "http://github.com/*",
                "https://github.com/*",
                "http://*.github.com/*",
                "https://*.github.com/*"
              ],
              "js": ["js/content.js"],
            "run_at": "document_end",
            "persistent": false
        }
    ],
    "web_accessible_resources": [
        "frame.html"
    ]
}
```

### content.js

```js
var elts = document.getElementsByClassName("new-discussion-timeline experiment-repo-nav")
var w = document.getElementsByClassName("repository-content ")

for (var i = 0; i < elts.length; i++) {
  elts[i].style['background-color'] = '#F0C';
  
  var iframe = document.createElement('iframe');
  // Must be declared at web_accessible_resources in manifest.json
  iframe.src = chrome.runtime.getURL('frame.html');

  // Some styles for a fancy sidebar
  iframe.style.cssText = 'width:100%;height:100%;'

  div.innerHTML = iframe

  elts[i].appendChild(iframe)
}
```

### popup.html

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Options</title>

</head>
<body>
    <div class="options">
        <button id="options--settings">Open App</button>
        <button id="options--text">atualiza texto</button>
    </div>
    <script src="js/jquery-3.2.1.min.js"></script>
    <script src="js/popup.js"></script>

</body>
</html>
```
### popup.js

```js
$('#options--settings').click(function(){
    chrome.tabs.create({'url': 'https://github.com/'})
})

$('#options--text').click(function(){
    var texto = "12:00";
    chrome.browserAction.setBadgeText({text: texto})
    chrome.browserAction.setBadgeBackgroundColor({ color: "#00FF00"})
})
```
### frame.html

```html
<h2>Displaying https://robwu.nl in a frame</h2>
<iframe width="1100" height="500" frameborder="0" src="https://www.youtube.com/embed/jVpiPCtbunw"></iframe>
```