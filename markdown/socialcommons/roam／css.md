- Colored tags for [[The 5 Essential Elements of Wellbeing]]
    - #physical
        - ```css
span.rm-page-ref[data-tag="physical"] {
    color: rgb(251,244,244) !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    line-height: 1em;
    border-radius: 5px 5px 5px 5px;
    position:relative;
	background: #1B42EA;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #76f264, #76f264);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #9C27B0, #DF6FF2); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

span.rm-page-ref[data-tag="physical"]:before {
    content: '🕺'
}```
    - #purpose
        - ```css
span.rm-page-ref[data-tag="purpose"] {
    color: white !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    line-height: 1em;
    border-radius: 5px 5px 5px 5px;
    position:relative;
	background: #FFEFBA;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #FFFFFF, #FFEFBA);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #C41511, #F46966); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

span.rm-page-ref[data-tag="purpose"]:before {
    content: '🧭'
}```
    - #community
        - ```css
span.rm-page-ref[data-tag="community"] {
    color: white !important;
  	padding: 3px 5px 3px 5px;
    font-size: 13px;
    line-height: 1em;
  	border-radius: 5px 5px 5px 5px;
    position:relative;
	background: #FFEFBA;  /* fallback for old browsers */
  	background: -webkit-linear-gradient(to right, #FFFFFF, #FFEFBA);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #0D71EB, #0d9deb);
}

span.rm-page-ref[data-tag="community"]:before {
    content: '🌏'
}```
    - #financial
        - ```css
span.rm-page-ref[data-tag="financial"] {
    color: white !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    line-height: 1em;
    border-radius: 5px 5px 5px 5px;
    position:relative;
	background: #FFEFBA;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #FFFFFF, #FFEFBA);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #397F3C, #3db841); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

span.rm-page-ref[data-tag="financial"]:before {
    content: '💰'
}```
    - #social
        - ```css
span.rm-page-ref[data-tag="social"] {
    color: #FFFFFF !important;
    padding: 3px 5px 3px 5px;
	font-size: 13px;
    line-height: 1em;
    border-radius: 5px 5px 5px 5px;
    position:relative;
	background: #FFEFBA;  /* fallback for old browsers */
	background: -webkit-linear-gradient(to right, #FFFFFF, #FFEFBA);  /* Chrome 10-25, Safari 5.1-6 */
	background: linear-gradient(to right, #D07E04, #e8a84a); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}

span.rm-page-ref[data-tag="social"]:before {
    content: '💞'
}```
- make block references more visible (from @joel-covid19)
    - The purpose of this is to allow in-line commenting on other people's comments to more clearly show visually which part is a "quote" that we are responding to, and which part is the "new speaker" speaking.

        - also note that, since this now provides a strong visual cue that something is a block, I'm taken the liberty of turning off the underlining as well, because it now seems redundant. 
    - CSS below:
        - ```css
/* turn off underlining */ 
.rm-block-ref{
    border-bottom: none;
}

/* recolor the block reference */

.rm-block-ref{
    background-color: #ffffe3;
}```
- subset of the [[Roaman Agora]]) (from @joel-covid19)
    - Variables
        - Colors
            - Black, White, Gray
                - ```css
:root {
  --cl-white:    #ffffff;
  --cl-gray-100: #f8f9faff; /*--cultured*/
  --cl-gray-200: #e9ecefff; /*--cultured-2*/
  --cl-gray-300: #dee2e6ff; /*--gainsboro*/
  --cl-gray-400: #ced4daff; /*--light-gray*/
  --cl-gray-500: #adb5bdff; /*--cadet-blue-crayola*/
  --cl-gray-600: #6c757dff; /*--slate-gray*/
  --cl-gray-700: #495057ff; /*--davys-grey*/
  --cl-gray-800: #343a40ff; /*--gunmetal*/
  --cl-gray-900: #212529ff; /*--charleston-green*/
  --cl-black:    #000000;
}```
    - Code
        - [[css/Daily Note Pages]]
            - #[[Change Log]]
                - ```css
span.rm-page-ref[data-tag="Change Log"] {
    background: var(--cl-gray-600);
    color: var(--cl-white);
    padding: 2px 5px 2px 5px;
    font-size: 13px;
    line-height: 1em;
    font-weight: 500;
    border-radius: 5px 5px 5px 5px;
    position:relative;
}

span.rm-page-ref[data-tag="Change Log"]:before {
    content: '📢'
}```
        - [[css/User Interface & Block Content]]
            - External Links
                - V2
                    - ```css
/*Aliases - internal & external*/
.rm-alias--external {
  color: var(--fg-link);
    text-decoration: none!important;
    border-bottom: 1px dashed;
}

.rm-alias--external:hover {
	color: var(--fg-link-hover);
    text-decoration: none!important;
    border-bottom: 1px dashed;
}

.rm-alias--external:after {
  content: ' ↗';```
