##Simple File Input
-----------
Simple File Input is a free jquery plugin to customise your file inputs ( upload fields ).

##Contribute
-----------  
If anyone could add something that will get this plugin better, please Feel free to contribute by forking then making a pull request.

#### Dependencies

jQuery : https://github.com/jquery/jquery

#### Compatibility
recent browsers such as :
IE 7+, Safari, Firefox & Chrome.
  
##Markup
-----------
```html
<input type="file" class="custom-input-class">
```

```js
$(document).ready(function(){
    $('.custom-input-class').simpleFileInput();
});
```

##Documentation
-----------

### Parameters

**placeholder:** `default:Pick your file`  
Basically it's like a placeholder, a text that shows up when there is no selected file yet (`default`). 

**wrapperClass :**   `default : sfi-container `  
This is the class used for the wrapper that wraps the customised file input.
Warning: if `wrapperClass`: is not `sfi-container` then you'll need to write your own css code, or at least change the one provided and get it adapted to your new class.
  
**validClass :** `default : .sfi-valid`  
If everything goas right, this class gets added to the wrapper and you can use it for CSS'ying.

**errorClass :** `default : .sfi-error`  
If a file with a wrong extension has been picked, this class gonna be added to the wrapper, so you can use it for CSS'ying.

**disabledClass :** `default : .sfi-disabled`  
If the input file is disabled on the html, you may need to give it a different style, that's why `.sfi-disabled` is there.



**buttonText :** `default : Pick your file`  
Used for the button as a visual text, in our CSS we've used text-indent which makes it invisible, that depends on your case, if it happens and you needed it, it's there :).

**allowedExts :** `default : false`  
Used to limit the accepted file types of the input, if you wanted to set some allowed extensions you'll need to add it as an array (`Ex : ['png', 'jpg', 'jpeg', 'gif']`)

**width :** `default : 300`  
This parameter can be `false`, this way the plugin would not set a width for the element, but if you do need a specific dimension you can use it.




### API

###### Callbacks

**onInit :**
Gets called during the initialisation of the plugin ( on each input );

**onError :** 
Gets called if the choosen file has a non-accepted extention / file type.

**onFileSelect :** 
Gets called when a file gets selected ( if the file doesn't respect the allowed extensions this callback won't be fired )
 
### CSS Classes

**.sfi-js  :**  
This class gets added to the *html* tag, and it's used on css for targeting the plugin's dom elements

**.sfi-wrapper  :**  
This class is used to wrap

**.sfi-filename  :**  
Set to the element that contains the file name.

**.sfi-trigger  :**  
Set to file input button, we've separated those to give much more freedom to stylise each part of the input.

**.sfi-error  :**  
Set to the wrapper when the choosen file has a wrong file type.

**.sfi-valid  :**  
Set to the wrapper when the a valid file gets selected.

**.sfi-disabled  :**  
Set to the wrapper when input file has the attribute disabled on it.
