# Tips-Js :bulb:

<p align="center">
  <img src ="http://i.imgur.com/dSkU3uC.png" />
</p>


## Disable right click on my web page, Disable view source, Disable developer tools
``` bash
<script language="javascript">
    window.oncontextmenu = function () { return false; };
    document.onkeydown = function(e){ if(event.keyCode == 123) {return false; } if(e.ctrlKey && e.shiftKey && e.keyCode == 'I'.charCodeAt(0)){return false;}if(e.ctrlKey && e.shiftKey && e.keyCode == 'J'.charCodeAt(0)){return false;}if(e.ctrlKey && e.keyCode == 'U'.charCodeAt(0)){return false;}}
</script>
```

## Automatically  Refresh DOM HTML
``` bash
<div id="re"></div>

<script type="text/javascript">
    setInterval(function () {
        $('#re').load(document.URL + ' #re');                  //Refresh 1 second
    }, 1000)
</script>
```
## Get Variable Javascript to Form HTML
``` bash
<form action="">
<input type="hidden" id="getNum" name="dataNum">
<input type="hidden" id="getString" name="dataString">
</form>

<script type="text/javascript">
var num = 100;
var str = 'hello';
     $(document).ready(function() {
          document.getElementById("getNum").value = num;
          document.getElementById("getString").value = str;
     });
</script>
```

