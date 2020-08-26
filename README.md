# JsGameHacks

This repo will contain all the games of browsers that I managed to break with pure javascript code.

## 10fastfingers.com
copy paste this code into the browser's console. (In Chrome: right click, inspect element and then change tab to "Console").
```javascript
const inputField = document.getElementById("inputfield");	
const ke = new KeyboardEvent("keyup", {
    		bubbles: true, cancelable: true, keyCode: 32
	});
const loopTime = 100;
setInterval(function(){
	inputField.focus();
	let word  = document.querySelector(".highlight").textContent;
	inputField.value = word;
	inputField.dispatchEvent(ke);
	
},loopTime);
