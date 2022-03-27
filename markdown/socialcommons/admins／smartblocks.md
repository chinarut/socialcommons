- {{[[roam/js]]}}
    - ```javascript
var existing = document.getElementById("roamjs-smartblocks-main");
if (!existing) {
  var extension = document.createElement("script");
  extension.src = "https://roamjs.com/smartblocks/main.js";
  extension.id = "roamjs-smartblocks-main";
  extension.async = true;
  extension.type = "text/javascript";
  document.getElementsByTagName("head")[0].appendChild(extension);
}
```
- #SmartBlock question index
    - <%J:```javascript
// finds notes missing from an index based on their starting prefix e.g. [[Evergreen]]/

return getMissingNotes("Q/","Questions");

function getMissingNotes(pagePrefix, indexPage){
  let ancestor = `[ 
  [(ancestor ?child ?parent)
   [?parent :block/children ?child]]
  [(ancestor ?child ?ancestor)
   [?parent :block/children ?child]
   (ancestor ?parent ?ancestor)]
]`;

var allPages = window.roamAlphaAPI.q(`
[:find ?name
  :in $ % ?tag
  :where
    [_ :node/title ?name]
    [(clojure.string/starts-with? ^String ?name ?tag)]]
]`, ancestor,pagePrefix);
  
var missingPages = window.roamAlphaAPI.q(`
[:find ?pages
  :in $ % ?container_title [?pages ...]
  :where
    [?container_page :node/title ?container_title]
    [?page :node/title ?pages]
    (not (ancestor ?container_block ?container_page)
         [?container_block :block/refs ?page])
]`, ancestor, indexPage,allPages.map((data, index) => {return `${data[0]}`}));
  
return missingPages.map((data, index) => {return `[[${data[0]}]]`});
}``` %>
- #SmartBlock proposition index
    - <%J:```javascript
// finds notes missing from an index based on their starting prefix e.g. [[Evergreen]]/

return getMissingNotes("P/","Propositions");

function getMissingNotes(pagePrefix, indexPage){
  let ancestor = `[ 
  [(ancestor ?child ?parent)
   [?parent :block/children ?child]]
  [(ancestor ?child ?ancestor)
   [?parent :block/children ?child]
   (ancestor ?parent ?ancestor)]
]`;

var allPages = window.roamAlphaAPI.q(`
[:find ?name
  :in $ % ?tag
  :where
    [_ :node/title ?name]
    [(clojure.string/starts-with? ^String ?name ?tag)]]
]`, ancestor,pagePrefix);
  
var missingPages = window.roamAlphaAPI.q(`
[:find ?pages
  :in $ % ?container_title [?pages ...]
  :where
    [?container_page :node/title ?container_title]
    [?page :node/title ?pages]
    (not (ancestor ?container_block ?container_page)
         [?container_block :block/refs ?page])
]`, ancestor, indexPage,allPages.map((data, index) => {return `${data[0]}`}));
  
return missingPages.map((data, index) => {return `[[${data[0]}]]`});
}``` %>
- #SmartBlock term index
    - <%J:```javascript
// finds notes missing from an index based on their starting prefix e.g. [[Evergreen]]/

return getMissingNotes("T/","Terms");

function getMissingNotes(pagePrefix, indexPage){
  let ancestor = `[ 
  [(ancestor ?child ?parent)
   [?parent :block/children ?child]]
  [(ancestor ?child ?ancestor)
   [?parent :block/children ?child]
   (ancestor ?parent ?ancestor)]
]`;

var allPages = window.roamAlphaAPI.q(`
[:find ?name
  :in $ % ?tag
  :where
    [_ :node/title ?name]
    [(clojure.string/starts-with? ^String ?name ?tag)]]
]`, ancestor,pagePrefix);
  
var missingPages = window.roamAlphaAPI.q(`
[:find ?pages
  :in $ % ?container_title [?pages ...]
  :where
    [?container_page :node/title ?container_title]
    [?page :node/title ?pages]
    (not (ancestor ?container_block ?container_page)
         [?container_block :block/refs ?page])
]`, ancestor, indexPage,allPages.map((data, index) => {return `${data[0]}`}));
  
return missingPages.map((data, index) => {return `[[${data[0]}]]`});
}``` %>
- #SmartBlock source index
    - <%J:```javascript
// finds notes missing from an index based on their starting prefix e.g. [[Evergreen]]/

return getMissingNotes("S/","Sources");

function getMissingNotes(pagePrefix, indexPage){
  let ancestor = `[ 
  [(ancestor ?child ?parent)
   [?parent :block/children ?child]]
  [(ancestor ?child ?ancestor)
   [?parent :block/children ?child]
   (ancestor ?parent ?ancestor)]
]`;

var allPages = window.roamAlphaAPI.q(`
[:find ?name
  :in $ % ?tag
  :where
    [_ :node/title ?name]
    [(clojure.string/starts-with? ^String ?name ?tag)]]
]`, ancestor,pagePrefix);
  
var missingPages = window.roamAlphaAPI.q(`
[:find ?pages
  :in $ % ?container_title [?pages ...]
  :where
    [?container_page :node/title ?container_title]
    [?page :node/title ?pages]
    (not (ancestor ?container_block ?container_page)
         [?container_block :block/refs ?page])
]`, ancestor, indexPage,allPages.map((data, index) => {return `${data[0]}`}));
  
return missingPages.map((data, index) => {return `[[${data[0]}]]`});
}``` %>
