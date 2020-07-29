# AutoTemperatureScript
This is an auto fill script for for daily self-check Temperature survey.

[設定]
需先將"在共享工作表中顯示"打開，如此一來在開啟ios的safari的共享的時候才可以看到腳本
![](/photo/config.gif)

[製作腳本]
加入動作->網頁->在網頁上執行javascript
![/photo/addScript.git]

[腳本內容]
第二行為工號，請務必記得改!
```javascript
document.getElementsByClassName("question-body clearfix notranslate")[0].getElementsByClassName("radio-button-input")[0].click();
document.getElementsByClassName("question-body clearfix notranslate")[1].getElementsByTagName("input")[0].value="xxxxxx"
document.getElementsByClassName("question-body clearfix notranslate")[2].getElementsByClassName("radio-button-input")[0].click()
document.getElementsByClassName("question-body clearfix notranslate")[3].getElementsByTagName("input")[0].value="35.4"
document.getElementsByClassName("question-body clearfix notranslate")[4].getElementsByClassName("radio-button-input")[1].click()
document.getElementsByClassName("question-body clearfix notranslate")[5].getElementsByClassName("radio-button-input")[0].click()
```

[如何使用]
再利用safari打開表單後，按下下方的分享按鈕，點選編輯動作，將你的腳本加入喜好項目後

就可以直接點選你所命名的腳本名稱，他就會幫你把標單填完，填完後別忘了檢查一下資料!
