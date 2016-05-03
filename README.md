#Captivate Tools  

I have been using SurveyGizmo since the middle of 2014. One night I was working on a script and I thought "What the hell am I doing re-creating something I have already built!". So with that I figured I would start documenting my scripts and processes and share them with fellow co-workers and other SurveyGizmo developers out there that have faced similar struggles in SurveyGizmo.  

##Validate Email Input Fields  
Captivate Instructions  
1. Create Text Input Field  
2. Adjust variable name to make more readable (ex:emailField,firstName,lastName,etc)  
3. Adjust Actions - On Focus Lost - Execute Javascript  

```javascript
function validateEmail(email) {
  if( /(.+)@(.+){2,}\.(.+){2,}/.test(email) ){
    alert('success');
  } else {
    alert('invalid email');
  }}

// Get value of Text Input Field using variable name
var emailField = window.cpAPIInterface.getVariableValue('emailField');

validateEmail(emailField);
```
