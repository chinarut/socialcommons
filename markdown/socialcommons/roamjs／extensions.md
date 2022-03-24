- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("roamjs-multiplayer-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/multiplayer/main.js";
  extension.id = "roamjs-multiplayer-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}```
