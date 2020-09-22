# AutoTemperatureScript
This is an auto fill script for for daily self-check Temperature survey.  
[demo]    
![](/photo/demo.gif)

[設定]
需先將"在共享工作表中顯示"打開，如此一來在開啟ios的safari的共享的時候才可以看到腳本
![](/photo/config.gif)

[製作腳本]
加入動作->網頁->在網頁上執行javascript  
![](/photo/addScript.gif)

[腳本內容]
第二行為工號，請務必記得改!
```javascript
document.getElementsByClassName("question-body clearfix notranslate")[0].getElementsByClassName("radio-button-input")[0].click();
document.getElementsByClassName("question-body clearfix notranslate")[1].getElementsByTagName("input")[0].value="xxxxxx"
document.getElementsByClassName("question-body clearfix notranslate")[2].getElementsByClassName("radio-button-input")[0].click()
let temperature = (Math.random() * (36.9 - 35) + 35).toFixed(1)
document.getElementsByClassName("question-body clearfix notranslate")[3].getElementsByTagName("input")[0].value=temperature
document.getElementsByClassName("question-body clearfix notranslate")[4].getElementsByClassName("radio-button-input")[1].click()
document.getElementsByClassName("question-body clearfix notranslate")[5].getElementsByClassName("radio-button-input")[0].click()
```
[random 說明]  
```javascript
/**
 * Get a random floating point number between `min` and `max`.
 * 
 * @param {number} min - min number
 * @param {number} max - max number
 * @return {number} a random floating point number
 */
function getRandomFloat(min, max) {
  return Math.random() * (max - min) + min;
}
```  
[如何使用]
再利用safari打開表單後，按下下方的分享按鈕  
![](/photo/surveyPage.jpg)  
往下滑點選"編輯動作"，將你的腳本加入喜好項目後，就可以直接點選你所命名的腳本名稱  
![](/photo/sharePage.jpg)  
腳本就會把標單填完，填完後別忘了檢查一下在按送出!
