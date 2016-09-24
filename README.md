#Combo.js - HTML Combo Box
<br/>
Turn a div into a combo box (select + input)

**Usage:**

```
<script src="https://rawgit.com/kofifus/New.js/master/new.js"></script>
<script src="https://rawgit.com/kofifus/Combo.js/master/combo.js"></script>

<div id="myCombo" style="width:200px;height:20px;"></div>

let div=document.getElementById('myCombo');
let combo=Combo.New(div);
```
<br/>
**Public interface:**

methods:

- Combo(div) - constructor 
- toggle(true/false/undefined) - show/hide/toggle combo
- focus() - move focus to the input area
- select(true/false/undefined) - select/deselect the text in the input field, default trure
- options(array/undefined) - sets/returns the array of options , default undefined
- getInputElement() - return the input element
- getSelectElement() - return the select element

getters:

- value - return value of input area

setters: 

- value=val&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- set value of input area
- onchange=f - f(event, self) will be called when Enter is pressed in the input field or selection changes<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e is a clone of the original event (onchange/onkeydown) with currentTarget set to the combo<br/>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;inside f, this==self, also as e is a clone of the original event there is no point in e.preventDefault it etc<br>
- onkeydown=f - f(event, self) will be called when keydown is pressed with
- onblur=f    - f(event, self) will be called on blur
<br/><br/>

**Example:**

http://stackoverflow.com/a/39036840/460084

