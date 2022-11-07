
 ## Form-Validation

\
It is important to validate form on website because user can add inappropriate values. Form validation normally occur at the server, after the client had entered all the necessary data and then pressed the Submit button. If the data entered by a client was incorrect or was simply missing,it send a request that the form is incorrect and submit again with correct information.
\
\
This process requires **HTML, CSS and JavaScript** code for proper validation. Here is the explanation of form-validation with JavaScript
\
\
Form validation usually perform two functions
\
\
**Basic Validation** : This validation checks that whether the client add values in the form or not. This can be easily checked using if-else statement. If the client did not add values and click submit this will provide an alert on the screen.

\
\
**Data format validation** : The entered data must be checked for correct form of value
\
\
**JavaScript first, last name validation and age verification**
```JavaScript
 if(firstName.length ===0 ){
        message+= 'First name is required\n';
        valid = false;
        count++;
    }

    if(lastName.length ===0){
        message+= 'Last name is required\n';
        valid = false;
        count++;
    }
    if(age.length===0){
        message+='Age is required\n';
        valid=false;
        count++;
    }else if(!isValid(Number(age))){
        message+='Age is required\n';
        valid=false;
    }

    
```
This is a quiet simple validation in which we check that whether this is an empty string or not and whether this a valid name or not. The code is provided above. In the age we check that the whether the entered value is number or not.
\
\
**Email-id verification** : For this we use regular expression to verify
```JavaScript
const emailRegex = /^(?=^.{8,}$)[-_A-Za-z0-9]+([_.-][a-zA-Z0-9]+)*@[A-Za-z0-9]+([.-][a-zA-Z0-9]+)*\.[A-Za-z]{2,}$/;
if(email.length===0){
        message+='Email is required\n';
        valid=false;
        count++;
    }else if(!emailRegex.test(email)){
        message+='A valid email is required';
        valid=false;
    }
```
The **emailRegex**  will check that whether tha data enetered is valid in terms of regular expression or not, if not, it will message an alert on window.
\
\
**Postal-code verification**
\
This is as same as email verification. It includes reg.expression and the validate the data.
```JavaScript
const postalRegex = /^[A-Za-z]\d[A-Za-z][ -]?\d[A-Za-z]\d$/;
if(postal.length===0){
    message+='Postal is required\n';
    valid=false;
    count++;
}else if(!postalRegex.test(postal)){
    message+='A valid postal is required';
    valid=false;
}
```
\
\
**Basic validation and submission of the form**
```JavaScript
if(count === 5){
    alert('Fields with * are required');
}else if (!valid){
    alert(message);
}else {
    alert('Form submitted');
    // form.submit();
}
```



### Demo

Click [here]( https://gurveerkaur1.github.io/Validation/ ) to check.

<br />

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)