# simpleDialog
simple bootstrap modal with multiple content options

![Open Dialog Window](https://github.com/ovaqlab/simpleDialog/blob/master/screenshot.png)

# Features
* Content from html elements or string  
* Backdrop enable and disable (optionsal)
* Buttons show/hide options (optional)
* Callback functions for success/confirm operations (optional)
* Working with bootstrap
* Responsive UI

# Usage

* Basic Usage 

```
<script type="text/javascript" src="/simpleDialog.js"></script>
<script type="text/javascript>
$.simpleDialog();
</script>
```
* simpleDialog with callback
```
<script type="text/javascript" src="/simpleDialog.js"></script>
<script type="text/javascript>
$.simpleDialog({},function(){
  alert("You confirmed");
});
</script>
```
* simpleDialog with options and callback

```
<script type="text/javascript" src="/simpleDialog.js"></script>
<script type="text/javascript">
  $.simpleDialog({
    title:"Confirm",
    message:"Do you want to continue?",
    confirmBtnText: "Yes! I'm Sure",
    closeBtnText: "Cancel",
    backdrop:true
  },function(){
  alert("You confirmed");
});
</script>
```
* simpleDialog with html element
```
<script type="text/javascript" src="/simpleDialog.js"></script>
<script type="text/javascript">
var html = '<div class="modal-header bg-white">'+
            '   <h4 class="modal-title capitalize-first-letter" id="modalHeader">Confirm</h4>'+
            '</div>'+
            '<div class="modal-body">'+
            '   <div class="row">'+
            '     <div class="col-md-12">Do you want to continue?</div>'+
            '   </div>'+
            '</div>';
  $.simpleDialog({
    modalContent: html,
    closeBtnText: "Cancel",
    backdrop:true
  },function(){
  alert("You confirmed");
});
</script>
```
You can pass either modal content or title and message. 
