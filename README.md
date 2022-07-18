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
    <script src="script/myOwnUI.Toaster.js" type="text/javascript"></script>
  </head>
  <body>
    <!-- Your page content -->
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

## Plugin parameters

### header

- Type: `String`
- Default: `"Header"`

To set toaster title.

### body

- Type: `String`
- Default: `"Please add some text to show here"`

To set toaster body content.

### type

- Type: `String`
- Default: `"info"`

You can change various type of toaster type here.

**Available options:**

  * info
  * warning
  * success
  * failure
  * unknown

### position

- Type: `String`
- Default: `"top"`

To set position of toaster

**Available options:**

  * top
  * top-right
  * right
  * bottom-right
  * bottom
  * bottom-left
  * left
  * top-left

### trigger

- Type: `String`
- Default: `"manual"`

To set the value for how toaster shows

**Available options:**

  * auto
  * manual
  
### presenceTimer

- Type: `Integer`
- Default: `5000`

To set duration of toaster keeps showing in second. 1000=1 sec.
  
### beforeWaitTimer

- Type: `Integer`
- Default: `100`

To set duration of toaster before showing. 1000=1 sec.
 
### autoClose

- Type: `Boolean`
- Default: `true`

After showing toaster, if you set this value to true, the toaster will automatically close based on presenceTimer.
If you set false, you should provide specific option to close toast.

### clickOnClose

- Type: `Boolean`
- Default: `false`

If you set this true, the toaster will get close immediately before auto close.

### hoverOnTimeFreeze

- Type: `Boolean`
- Default: `true`

If you set this true, the toaster timeout timer will freeze while hovering on toaster. The timer will resume after moving away from toaster.

### animateWhenShowAs

- Type: `String`
- Default: `"fade"`

To set how animate perform while toaster showing.

**Available options:**

  * fade
  * hide

### animateWhenHideAs

- Type: `String`
- Default: `"fade"`

To set how animate perform while toaster hiding.

**Available options:**

  * fade
  * hide
