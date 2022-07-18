# myOwnUIToaster

This is one of package from myOwnUI and jQuery plugin.

## Demo

For demo, please view this page [https://siva7170.github.io/myOwnUIToaster/](https://siva7170.github.io/myOwnUIToaster/)

## Getting Started

This plugin is work with jQuery. So, you need below requirements to work with this myOwnUIToaster

### Prerequisites

* Latest jQuery

* `myOwnUI.Toaster.css`

* `myOwnUI.Toaster.js`

### Initialization

Place "myOwnUI.Toaster.css" and latest jQuery above the end head tag and place "myOwnUI.Toaster.js" above the end body tag.

```html
<html>
  <head>
    <link rel="stylesheet" href="css/myOwnUI.Toaster.css" type="text/css"/>
    <script src="script/jquery-3.6.0.min.js" type="text/javascript"></script> <!-- Please update with latest jQuery -->
  </head>
  <body>
    <!-- Your page content -->
    <script src="script/myOwnUI.Toaster.js" type="text/javascript"></script>
  </body>
</html>
```

## Usage

Below code is sample for how to use it. Please see methods and its functionalities below sections.

```html
<html>
<head>
    <link rel="stylesheet" href="css/myOwnUI.Toaster.css" type="text/css"/>
    <script src="script/jquery-3.6.0.min.js" type="text/javascript"></script> <!-- Please update with latest jQuery -->
    <script type="text/javascript" src="script/myOwnUI.Toaster.js"></script>
</head>
<body>
  <button id="showToaster">Show</button>&nbsp;<button id="hideToaster">Hide</button>
        <script>
        $(document).ready(function(e){
            let myOwnUIT=undefined;
            $("#showToaster").on("click",function (){
                myOwnUIT=$.myOwnUIToaster({
                    header:"Title",
                    body:"This is test message",
                    type:"info",
                    position:"top-right",
                    presenceTimer:5000,
                    beforeWaitTimer: 300,
                    trigger:"auto",
                    animateWhenShowAs: "fade",
                    animateWhenHideAs: "fade",
                    hoverOnTimeFreeze:true,
                    autoClose: true,
                    clickOnClose: false
                });
            });

            $("#hideToaster").on("click",function (){
                if(myOwnUIT!==undefined){
                    myOwnUIT.close();
                }
            });
        });
    </script>
</body>
</html>
```

## Methods

### show

- Type: `method`

To show toaster, please use `show` method. 

```
    <script>
    //----------------  
       $(document).ready(function(e){
            let myOwnUIT=undefined;
            myOwnUIT=$.myOwnUIToaster({
                    header:"Title",
                    body:"This is test message",
                    type:"info",
                    position:"top-right",
                    presenceTimer:5000,
                    beforeWaitTimer: 300,
                    trigger:"manual",
                    animateWhenShowAs: "fade",
                    animateWhenHideAs: "fade",
                    hoverOnTimeFreeze:true,
                    autoClose: true,
                    clickOnClose: false
            });
            
            $("#showToaster").on("click",function (){
                 myOwnUIT.show();
            });
        });
    //----------------  
    </script>
```

### close

- Type: `method`

To close toaster, please use `close` methods. 

```
    <script>
    //----------------  
      $(document).ready(function(e){
            let myOwnUIT=undefined;
            myOwnUIT=$.myOwnUIToaster({
                    header:"Title",
                    body:"This is test message",
                    type:"info",
                    position:"top-right",
                    presenceTimer:5000,
                    beforeWaitTimer: 300,
                    trigger:"manual",
                    animateWhenShowAs: "fade",
                    animateWhenHideAs: "fade",
                    hoverOnTimeFreeze:true,
                    autoClose: true,
                    clickOnClose: false
            });
            
            $("#showToaster").on("click",function (){
                 myOwnUIT.show();
            });
            
            $("#hideToaster").on("click",function (){
                if(myOwnUIT!==undefined){
                    myOwnUIT.close();
                }
            });
        });
    //----------------  
    </script>
```
